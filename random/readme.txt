Use : 

- biên dịch driver và add driver vào nhân hệ thống
	+ cd to this directory
	+ Run make (build .ko file)
	+ Run sudo insmod randomModule.ko (add modules)
	+ file modules duoc luu tru lai : /dev/randomDevice

- test chuong trinh : gcc test.c -o test01 && sudo ./test01
