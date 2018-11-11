|ST|state Name|opcode_rdy|opcode[7:0]|meta_busy|tx_busy|full|empty|Run|read_match|delay_match|reg_out|valid_out||NS|Next Name||load_counter|data_meta_mux|begin_meta_transmit|send_id|en|rnw|clear|hold_window|edge_capture|arm|load_trigs|en_cnt|clr_cnt|wr_en|reg_sel|reset|
|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|
|0|IDLE|0|XXXXXXXX|X|X|X|X|X|X|X|X|X||0|IDLE||0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|1|
|0|IDLE|1|XXXXXXXX|X|X|X|X|X|X|X|X|X||1|CMD_RECIEVED||0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|1|
|1|CMD_RECIEVED|X|0000_0000|X|X|X|X|X|X|X|X|X||2|RESET||0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|#reset state
|1|CMD_RECIEVED|X|0000_0001|X|X|X|X|X|X|X|X|X||4|ARM||0|0|0|0|0|0|1|0|0|1|0|0|1|0|0|1|#arm basic trigger
|1|CMD_RECIEVED|X|0000_0010|X|X|X|X|X|X|X|X|X||3|META_WAIT||0|0|1|1|0|0|0|0|0|0|0|0|0|0|0|1|
|1|CMD_RECIEVED|X|0000_0011|X|X|X|X|X|X|X|X|X||0|IDLE||0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|1|
|1|CMD_RECIEVED|X|0000_0100|X|X|X|X|X|X|X|X|X||3|META_WAIT||0|0|1|0|0|0|0|0|0|0|0|0|0|0|0|1|
|1|CMD_RECIEVED|X|0000_0101|X|X|X|X|X|X|X|X|X||?|UNSURE||0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|1|
|1|CMD_RECIEVED|X|0000_0110|X|X|X|X|X|X|X|X|X||0|IDLE||0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|1|
|1|CMD_RECIEVED|X|0000_0111|X|X|X|X|X|X|X|X|X||?|UNSURE||0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|1|
|1|CMD_RECIEVED|X|0000_1000|X|X|X|X|X|X|X|X|X||?|UNSURE||0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|1|
|1|CMD_RECIEVED|X|0000_1001|X|X|X|X|X|X|X|X|X||0|IDLE||0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|1|
|1|CMD_RECIEVED|X|0000_101X|X|X|X|X|X|X|X|X|X||0|IDLE||0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|1|
|1|CMD_RECIEVED|X|0000_110X|X|X|X|X|X|X|X|X|X||0|IDLE||0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|1|
|1|CMD_RECIEVED|X|0000_111X|X|X|X|X|X|X|X|X|X||0|IDLE||0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|1|
|1|CMD_RECIEVED|X|XXX1_XXXX|X|X|X|X|X|X|X|X|X||0|IDLE||0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|1|
|1|CMD_RECIEVED|X|XX1X_XXXX|X|X|X|X|X|X|X|X|X||0|IDLE||0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|1|
|1|CMD_RECIEVED|X|1000_0000|X|X|X|X|X|X|X|X|X||0|IDLE||1|0|0|0|0|0|0|0|0|0|0|0|0|0|0|1|#load sampler
|1|CMD_RECIEVED|X|1000_0001|X|X|X|X|X|X|X|X|X||0|IDLE||0|0|0|0|0|0|0|0|0|0|0|0|0|1|0|1|#TODO: change read/delay for dual entry
|1|CMD_RECIEVED|X|1100_0000|X|X|X|X|X|X|X|X|X||0|IDLE||0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|1|#set trigger mask
|1|CMD_RECIEVED|X|1100_0001|X|X|X|X|X|X|X|X|X||0|IDLE||0|0|0|0|0|0|0|0|0|0|1|0|0|0|0|1|#trigger value
|1|CMD_RECIEVED|X|1XXX_XX1X|X|X|X|X|X|X|X|X|X||0|IDLE||0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|1|