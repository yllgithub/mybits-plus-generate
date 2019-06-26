# mybits-plus-generate
mybatis plus 生成器
 
1.修改 BASE_NAME 代表你的项目名称。<br/>

2.设置数据库 <br/>

    DataSourceConfig dsc = new DataSourceConfig();
    dsc.setUrl("jdbc:mysql://ip/database?useUnicode=true&characterEncoding=utf8");
    dsc.setDriverName("com.mysql.jdbc.Driver");
    dsc.setUsername("用户名称");
    dsc.setPassword("密码");
    mpg.setDataSource(dsc);
    
 3.设置包名 <br/>

    PackageConfig pc = new PackageConfig();
    pc.setParent("com.jyb." + BASE_NAME);
    pc.setEntity("api.model");
    pc.setMapper("provider.dao");
    pc.setService("api.service");
    pc.setServiceImpl("provider.service.impl");
    pc.setController("consumer.controller");
    mpg.setPackageInfo(pc);

  4.运行main方法 ，输入表名称，回车，就会在项目的根目录下生成一个src文件夹。 <br/>

