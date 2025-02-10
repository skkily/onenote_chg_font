#!/bin/bash

set -e

msyh_files=("msyh.ttc" "msyhbd.ttc" "msyhl.ttc")
calibril_files=("Calibri.ttf" "Calibrib.ttf" "calibril.ttf")

change_msyh()
{
	for i in {0..2}; do
		echo "cp ${msyh_files[i]} to ${calibril_files[i]}"
		cp ${msyh_files[i]} ${calibril_files[i]}
	done
}

rename_calibri()
{
	for i in `find . \( -name 'calibri*ttf' -o -name 'Calibri*ttf' \)`; do
		[ ! -f ${i}.save ] && {
			echo "mv ${i} to ${i}.save"
			mv ${i} ${i}.save
		}
	done
}

restore_calibri()
{
	for i in `find . -name '*ttf.save'`; do
		target_name=`echo ${i} | awk -F'.' '{print $1"."$2"."$3}'`
		echo "mv ${i} to ${target_name}"
		mv ${i} ${target_name}
	done
}

cd /Applications/Microsoft\ OneNote.app/Contents/Resources/DFonts

[ "$1" == "restore" ] && { restore_calibri; echo "restore ok"; exit 0; }
rename_calibri
change_msyh
echo "change ok"
exit 0
