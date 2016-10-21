
# 建表demo
```
CREATE TABLE `user_base` (
  `user_id` int(11) unsigned NOT NULL AUTO_INCREMENT COMMENT '用户ID',
  `user_name` varchar(40) NOT NULL COMMENT '用户名',
  `user_nick` varchar(40) NOT NULL COMMENT '用户昵称',
  `user_sex` tinyint(4) unsigned NOT NULL DEFAULT '0' COMMENT '性别 0保密，1男，2女',
  `user_email` varchar(40) NOT NULL COMMENT '用户邮箱',
  `user_level` smallint(3) unsigned NOT NULL DEFAULT '0' COMMENT '编辑给用户定位的级别：0-默认，1-最高级别',
  `user_rank` varchar(40) NOT NULL COMMENT '用户头衔',
  `editor_pic` text NOT NULL COMMENT '编辑添加的头像',
  `user_blog_tpl` mediumint(6) unsigned NOT NULL DEFAULT '1' COMMENT '用户博客模板',
  `user_pic` varchar(200) NOT NULL DEFAULT '' COMMENT '用户头像',
  `blog_name` varchar(40) NOT NULL COMMENT '博客名称',
  `group_id` mediumint(6) unsigned NOT NULL DEFAULT '1' COMMENT '用户组ID',
  `db_id` mediumint(6) unsigned NOT NULL COMMENT '用户分库信息',
  `ywt_id` varchar(32) NOT NULL COMMENT '一网通ID',
  `is_audit` tinyint(1) unsigned NOT NULL DEFAULT '0' COMMENT '是否通过审核：0-未通过，1-已通过',
  `is_pending` tinyint(1) unsigned NOT NULL DEFAULT '0' COMMENT '0：未待定，1：已待定',
  `is_lock` tinyint(1) unsigned NOT NULL DEFAULT '0' COMMENT '0：未锁定，1：已锁定',
  `is_del` tinyint(1) unsigned NOT NULL DEFAULT '0' COMMENT '是否被删除：0-未删除，1-已删除',
  `is_email_checked` tinyint(1) unsigned NOT NULL DEFAULT '0' COMMENT 'Email是否通过验证:''0''没有通过验证,''1''为通过验证',
  `is_avatar_uploaded` tinyint(1) unsigned NOT NULL DEFAULT '0' COMMENT '0未上传，1已上传',
  `is_show_reward` tinyint(1) unsigned NOT NULL DEFAULT '0' COMMENT '0->不显示打赏，1->显示打赏',
  `user_pass` char(32) NOT NULL COMMENT '用户密码',
  `register_time` int(10) unsigned NOT NULL DEFAULT '0' COMMENT '注册时间',
  `register_ip` char(15) NOT NULL COMMENT '注册IP',
  `reg_email` varchar(40) NOT NULL COMMENT '注册邮箱',
  `last_update_time` int(10) unsigned NOT NULL DEFAULT '0' COMMENT '最后更新资料时间',
  `privacy` text NOT NULL COMMENT '导数据用，实际不用他',
  PRIMARY KEY (`user_id`),
  KEY `user_name` (`user_name`)
) ENGINE=MyISAM AUTO_INCREMENT=59202344 DEFAULT CHARSET=utf8 COMMENT='用户表';

```