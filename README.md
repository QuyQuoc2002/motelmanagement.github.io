# Motel-Management
	Ý tượng
xây dựng module quản lí phòng trọ
Web app:
	+ lưu trữ mẫu hợp đồng đặt cọc: phòng cọc, tiền cọc, ngày cọc, hạn cọc
	+ lưu trữ mẫu hợp đồng cho thuê: 
	+ quản lí lượng phòng loại phòng, tầng,
	+ quản lí check in check out người thuê, lượng người thuê trong một phòng
	  biển số xe, bao nhiêu xe đạp bao nhiêu xe máy
	+ quản lí nhân sự trong tòa trọ (option)
	+ quản lí các khoản chi: thời gian, số tiền, mô tả
	+ xem trạng thái phòng: 2, 3 người ở, đang trống, đang được cọc
	+ điền thông tin điện nước, tính tiền thuê trọ
	+ khi vào xem thông tin phòng nếu:
		- trống: hiện phòng đang trống
		- có người ở: hiện thông tin những người ở trong phòng, phương tiện từng người...
		- đặt cọc: hiện ngày đặt cọc, số tiền, ngày hết hạn cọc
	+ nhân viên lấy số điện số nước thì có thể chỉnh sửa trong ngày
	staff chỉ có thể lấy số điện số nước, phòng nào đang trống hoặc đang cọc thì ko cho lấy
	
	
table:
	RoomStatus:
		+ room_status_id
		+ status: (đang cho thuê, còn trống, đang đặt cọc)
		+ icon (option)
	Floor:
		+ floor_id
		+ floor_number
	RoomType:
		+ room_type_id
		+ max_mem_ber
		+ price
		+ area
	Room:
		+ room_id
		+ room_name
		+ room_type_id
		+ floor_id
		+ room_status_id
	Member:
		+ member_id
		+ citizen_identification_number
		+ name
		+ dob
		+ img
		+ countryside
		+ phone_number
		+ parent_phone_number
		+ room_id
	Staff: (liên hệ với thợ điện nước bên ngoài, thông tin nhân viên trong tòa)
		+ staff_id
		+ citizen_identification_number
		+ name
		+ dob
		+ img
		+ countryside
		+ phone_number
		+ salary
		+ role_name
	payment
		+ id_payment
		+ room_id
		+ water_index_previous_update
		+ day_update_previous_update
		+ electric_index_this_update
		+ electric_update_this_update
		+ moto_number
		+ moto_parking_fee	
		+ bike_number
		+ bike_parking_fee	
		+ total_payment
	vehical
		+ vehical_id
		+ unit_fee_id
		+ member_id
		+ brand_name
		+ license_plates_number
	Unit_fee
		+ unit_fee_id
		+ name 
		+ price
		+ description
		
		
	User, User_Role, Role
