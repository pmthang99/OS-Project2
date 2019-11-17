1/ Hướng dẫn sử dụng:

   - Biên dịch hook và nạp hook vào kernel:
	+ cd to thís 
	+ run make
	+ run sudo insmod hook.ko
	+ sudo lsmod | grep hook to check.
	+ tới bước này thì khi gọi syscall write và open thì sẽ tự gọi custom syscall
	+ Để gỡ driver sử dụng cú pháp: "sudo rmmod hook" 
   - Sử dụng:
	+ Sau khi nạp thành công và thay thế syscall thì chúng ta đã hook thành công
	+ Syscall open => ghi vào dmesg tên tiến trình mở file và tên file được mở. 
	+ Syscall write => ghi vào dmesg tên tiến trình, tên file bị ghi và số byte được ghi. 
	
2/ Ghi chú:

   - Chương trình hook được test ở linux kernel version 4.7
   - Chương trình được cài đặt trên phiên bản ubutu 18.04
