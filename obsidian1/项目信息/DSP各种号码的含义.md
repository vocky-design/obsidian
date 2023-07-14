```c
/* DSP系统命令:0-100 */
0{CMD_DSP_CMD_SERVER_OK, test_dsp_cmd_server},						//测试DSP cmd 服务开启
1{CMD_DSP_PRINT_DIRECT_CTL, cmd_dsp_print_ctrl},						//控制dsp打印输出方向
2{CMD_SET_LOG_LEVEL, cmd_set_log_level},								//设置日志打印等级
3{CMD_START_BINO_DEV, cmd_dsp_start_bino},							//启动双目设备
4{CMD_STOP_BINO_DEV, cmd_dsp_stop_bino},								//停止双目设备
5{CMD_START_CODE_READER_DEV, cmd_start_code_reader},					//启动读码sensor
6{CMD_GET_PUB_MSG_SIZE, cmd_get_pub_msg_size},						//获取发布信息的大小
7{CMD_GET_VER, cmd_get_version},										//获取版本信息
8{CMD_RECORD_INSTRUMENT, cmd_record_instrument},						//记录插桩信息
9{CMD_START_SUB_DSP_MSG, cmd_start_sub_dsp_msg},						//开始订阅DSP发布信息
10{CMD_STOP_SUB_DSP_MSG, cmd_stop_sub_dsp_msg},						//停止订阅DSP发布信息

/* 双目相关命令:100-200   */
100{CMD_SET_BINO_CTL_PARAM, cmd_set_bino_ctl_param},					//设置双目相关参数(散斑灯状态)
101{CMD_GET_BINO_CTL_PARAM, cmd_get_bino_ctl_param},					//获取双目相关参数(散斑灯状态)
102{CMD_GET_BINO_INTRINSICS, cmd_get_bino_intrinsics},					//获取双目内参
103{CMD_GET_BINO_BASELINE, cmd_get_bino_baseline},						//获取双目左右相机的距离
104{CMD_GET_BINO_COLOR_INTRINSICS, cmd_get_bino_color_intrinsics},		//获取双目彩色相机内参
105{CMD_GET_BINO_COLOR_EXTRINSICS, cmd_get_bino_color_extrinsics},		//获取双目彩色相机外参
106{CMD_DUMP_BINO_IMG, cmd_dump_bino_img},								//保存双目图像到本地
107{CMD_GET_BINO_OPERATIION_INFO, cmd_get_bino_operation_info},		//获取运行双目设备信息

/* 读码相关命令:200-300   */
200{CMD_LOAD_DSP_CORE, cmd_load_dsp_core},								//装载dsp核镜像 
201{CMD_UNLOAD_DSP_CORE, cmd_unload_dsp_core},							//卸载dsp核镜像
202{CMD_MALLOC_SHARE_MAP_BUF, cmd_malloc_map_buf},						//分配地图共享内存
203{CMD_REALEASE_SHARE_MAP_BUF, cmd_free_map_buf},						//释放地图共享内存
204{CMD_SET_AND_START_CODE_READER_MRSE, cmd_set_and_start_hk_mrse},	//首次启动或者销毁重启引擎
205{CMD_SUSPEND_CODE_READER_MRSE, cmd_suspend_hk_mrse},				//暂停引擎
206{CMD_WAKEUP_CODE_READER_MRSE, cmd_wakeup_hk_mrse},					//唤醒引擎
207{CMD_GET_CODE_READER_MRSE_KEY, cmd_get_mrse_key_config},			//动态获取引擎算法库参数
208{CMD_SET_CODE_READER_MRSE_KEY, cmd_set_mrse_key_config},			//动态设置引擎算法库参数
209{CMD_UPDATE_CODE_READER_LOCATION, cmd_update_loc_info},				//更新位置信息
210{CMD_TRIGGER_CODE_READER_MAPPING, cmd_trigger_mapping},				//触发建图模式
211{CMD_GET_CODE_READER_LOC_RESULT_SIZE, cmd_get_loc_result_size},		//获取定位结果输入尺寸
212{CMD_SET_CODE_READER_INNER_PARAM_MAT, cmd_set_inner_param_mat},		//设置内参矩阵(坐标转换、标定畸变)
213{CMD_SET_CODE_READER_CTL_PARAM, cmd_set_ctl_param},					//设置dev相关参数(sensor曝光，增益等)
214{CMD_GET_CODE_READER_CTL_PARAM, cmd_get_ctl_param},					//获取dev相关参数(sensor曝光，增益等)
215{CMD_SET_SENSOR_ROI, cmd_set_sensor_roi},							//设置sensor的ROI开窗参数 
216{CMD_SET_SENSOR_SUSPEND, cmd_set_sensor_suspend},					//控制sensor暂停
217{CMD_SET_SENSOR_RESUME, cmd_set_sensor_resume},						//控制sensor启动
218{CMD_DUMP_CODE_READER_IMG, cmd_dump_code_reader_img},				//保存读码图像到本地
219{CMD_RECORD_MRSE_INNER_LOG, cmd_record_mrse_inner_log},				//记录引擎内部日志到DSP日志
220{CMD_RESET_DSP_CORE, cmd_reset_dsp_core},							//复位DSP核
221{CMD_INSERT_USER_IMG, cmd_insert_user_img},							//插入用户图像给引擎处理
222{CMD_SET_CODE_READER_SCALE, cmd_set_code_reader_scale},				//设置读码图像的缩放比例
223{CMD_CODE_READER_MAPPING_CTRL, cmd_ctrl_vl_mapping},				//控制连续纹理建图

/* 音频相关命令:300-400   */
300{CMD_AUDIO_PLAY, cmd_audio_play},									//启动音频播放
301{CMD_AUDIO_SET_VOLUME, cmd_audio_set_volume},						//设置音频输出音量
302{CMD_AUDIO_GET_VOLUME, cmd_audio_get_volume},						//获取音频输出音量
303{CMD_AUDIO_STOP, cmd_audio_suspend_play},								//停止音频播放
304{CMD_AUDIO_RESTART, cmd_audio_restart_play},						//停止后重新开始音频播放
```

