# my_f
m
CREATE TABLE PadMenu_AuthManage(
MenuId varchar(64) NOT NULL,
MenuName varchar(128),
ParentMenuId varchar(64),
ParentMenuName varchar(64)
);

COMMENT ON TABLE PadMenu_AuthManage IS '平板菜单权限管理表';
COMMENT ON COLUMN PadMenu_AuthManage.MenuId IS '菜单ID';
COMMENT ON COLUMN PadMenu_AuthManage.MenuName IS '菜单名称';
COMMENT ON COLUMN PadMenu_AuthManage.ParentMenuId IS '父级菜单ID';
COMMENT ON COLUMN PadMenu_AuthManage.ParentMenuName IS '父级菜单名称';
