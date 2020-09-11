## `openjdk:16-ea-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:d7e99f2033fe1703348be973cef5d1fb01d1065d7e8ea6682f3ca9f919a536af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1457; amd64

### `openjdk:16-ea-jdk-nanoserver` - windows version 10.0.17763.1457; amd64

```console
$ docker pull openjdk@sha256:ba72e9dd1e2b2805878ccfb39fd9a17e7cafbf32cb1e59f00e8ae283d7ac1401
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.0 MB (297043092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d9e3bdbb3afad86dad3c1a37947a9f3e7355e87b84ea6723ede0162bb2a6798`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 02 Sep 2020 12:08:18 GMT
RUN Apply image 1809-amd64
# Tue, 08 Sep 2020 20:13:38 GMT
SHELL [cmd /s /c]
# Tue, 08 Sep 2020 20:13:38 GMT
ENV JAVA_HOME=C:\openjdk-16
# Tue, 08 Sep 2020 20:13:39 GMT
USER ContainerAdministrator
# Tue, 08 Sep 2020 20:13:53 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH%
# Tue, 08 Sep 2020 20:13:54 GMT
USER ContainerUser
# Fri, 11 Sep 2020 22:51:13 GMT
ENV JAVA_VERSION=16-ea+15
# Fri, 11 Sep 2020 22:51:53 GMT
COPY dir:6134b2d11b910440d568d97884bb85bfa4b08d7474e3194e66a08686ae653310 in C:\openjdk-16 
# Fri, 11 Sep 2020 22:52:20 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version
# Fri, 11 Sep 2020 22:52:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ecf9bb62dc6eedea9fd367628f8715dea75b7d2053afa4b5121e7809aa692139`  
		Size: 101.2 MB (101239122 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f72ec155bceaba8b4a5cdbd7aa79586c7296a801af5364a691c46191c910e2da`  
		Last Modified: Tue, 08 Sep 2020 22:29:01 GMT  
		Size: 864.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42b2192657885f813dd6fa78d8ba65d02e35934c0c45121f5cb3004298998876`  
		Last Modified: Tue, 08 Sep 2020 22:28:59 GMT  
		Size: 866.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffe914594cd5b7b9a0b5c0080fe6c643b51eecedb3197955dbea30a0005a9132`  
		Last Modified: Tue, 08 Sep 2020 22:28:59 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4324dc65079aab4e95e3a823193385145a250bbb9e13cd9c5e02a35844069217`  
		Last Modified: Tue, 08 Sep 2020 22:29:00 GMT  
		Size: 65.1 KB (65142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bee2eb45cc55aae1760d1937d9de7b70abd95c9488b97a8288d08b472684fb5`  
		Last Modified: Tue, 08 Sep 2020 22:28:57 GMT  
		Size: 862.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c537a6d14a514c0850668fe776bafec3d2ae7b57e201ee11bd79fba2b987af99`  
		Last Modified: Fri, 11 Sep 2020 23:00:08 GMT  
		Size: 885.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85aa4116c62d89fbed868504f1c89aaf5c77e6db6dd1eb6885bb115918e467aa`  
		Last Modified: Fri, 11 Sep 2020 23:01:25 GMT  
		Size: 192.2 MB (192242962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f4048c9584b6901062f1fa872f9321bba415c8b9022deadd1779fe451b4cdbd`  
		Last Modified: Fri, 11 Sep 2020 23:00:29 GMT  
		Size: 3.5 MB (3490611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:661b05b449e8e303d850a1b2da97003b1495bec75ef4783fc5f8e2accf06fc10`  
		Last Modified: Fri, 11 Sep 2020 23:00:15 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
