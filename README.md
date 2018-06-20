# my_f
m
-------------------------------pad菜单管理--------------
--二级菜单
update RULE 
 set ruledef= 'EquiAdd,IpadAndPacMgmt,PadMenuManage'
 where  MODULEID='mgmt' and RULEID='equimaint' and ruletype='MenuTreeDef';
 
--三级菜单
INSERT INTO RULE(RULETYPE, RULEID, MODULEID, RULEDEF, RULESCRIPT, USERTYPE, PRDGRPID, PRDID, DESCRIPTION, MAINTAINTAG, STATE)
VALUES('Menu', 'PadMenuManage', 'mgmt', 'PadMenuManage,padMenuManage.do', NULL, '3', NULL, NULL, NULL, NULL, NULL);

INSERT INTO PRODUCT(PRDID, MODULEID, PRDNAME, PRDGRPID)
VALUES('PadMenuManage', 'mgmt', 'pad菜单管理', 'equimgmt');

INSERT INTO BANKPGP (  BANKSEQ,PRDID, PRDGRPID,PRDGRPSTATE ) 
VALUES  (1,'PadMenuManage','equimgmt','0');

INSERT INTO productgroupproduct (  PRDID, PRDGRPID) 
VALUES  ('PadMenuManage','equimgmt');

INSERT INTO BANKROLEPGP (ROLEID, BANKSEQ, PRDID,PRDGRPID)   VALUES ('sysAdmin','1','PadMenuManage','equimgmt');

INSERT INTO producttrs(Prdid,Transcode) values('PadMenuManage','padMenuManage');

INSERT INTO producttrs(Prdid,Transcode) values('PadMenuManage','padMenuManagePre');

---------

INSERT INTO producttrs(Prdid,Transcode) values('PadMenuManage','padMenuEdit');

INSERT INTO producttrs(Prdid,Transcode) values('PadMenuManage','PadMenuAuthUpConfirm');

INSERT INTO producttrs(Prdid,Transcode) values('PadMenuManage','PadMenuAuthUp');

INSERT INTO producttrs(Prdid,Transcode) values('PadMenuManage','tellerPadAuthQuery');


-------------------------------
