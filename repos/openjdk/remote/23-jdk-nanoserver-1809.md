## `openjdk:23-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:121633028fd4681267c642b7bfcfc6e40f8489cd3e87270e506c219a5f937707
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5122; amd64

### `openjdk:23-jdk-nanoserver-1809` - windows version 10.0.17763.5122; amd64

```console
$ docker pull openjdk@sha256:c8b7002f65f23d900ba259c341d902f1b026dc1da8d00515dd8e21084afce381
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.8 MB (305822628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:988f6fb1fb4d473fbbb6e50f462251b1ad58102b7304c7126878e0eed224990f`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 09 Nov 2023 17:21:05 GMT
RUN Apply image 10.0.17763.5122
# Thu, 16 Nov 2023 01:41:12 GMT
SHELL [cmd /s /c]
# Tue, 12 Dec 2023 20:19:41 GMT
ENV JAVA_HOME=C:\openjdk-23
# Tue, 12 Dec 2023 20:19:41 GMT
USER ContainerAdministrator
# Tue, 12 Dec 2023 20:19:53 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 12 Dec 2023 20:19:54 GMT
USER ContainerUser
# Tue, 12 Dec 2023 20:19:54 GMT
ENV JAVA_VERSION=23-ea+1
# Tue, 12 Dec 2023 20:20:08 GMT
COPY dir:c1af40c3dd3a5b960ebf976dd48a5f1482d7c7d93cf37ee2fe2c47c56a119861 in C:\openjdk-23 
# Tue, 12 Dec 2023 20:20:19 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 12 Dec 2023 20:20:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:24e10ec0ecb89022cf68752b9f9196dcf2f423f9589b14401693fb2a1b3de37f`  
		Last Modified: Tue, 14 Nov 2023 22:06:25 GMT  
		Size: 104.5 MB (104497517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e5c133738aab79d4c21c47e77cb838e2d00166f5e3e2632177622f67488259`  
		Last Modified: Thu, 16 Nov 2023 02:28:08 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f20feb8baca86a7657eeb866d6aa5e462f07ebb8265637d16fd79bfe3e7e40e7`  
		Last Modified: Tue, 12 Dec 2023 20:23:08 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3398dbdabcce695e596b039c6b3c7aef18ac70037ab8f9b5b908c31c425c9179`  
		Last Modified: Tue, 12 Dec 2023 20:23:08 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8740d7b464b9b28e4d6438871a8b24bb6bf0b14544409bed32dafea732e34c2c`  
		Last Modified: Tue, 12 Dec 2023 20:23:08 GMT  
		Size: 68.5 KB (68452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:536b463060f59a72464e6d84457b36b6ecbbb6c9feee1ebe282ca78e27c6d405`  
		Last Modified: Tue, 12 Dec 2023 20:23:06 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e6f1929d35ebfed50ed104fc072f5afbd336b1a967fe26444e43043bf282fb2`  
		Last Modified: Tue, 12 Dec 2023 20:23:06 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee21b4e64fcd7d1cbf2f337f90aca865191252040e4990c905225c0e8dd1b4e0`  
		Last Modified: Tue, 12 Dec 2023 20:23:23 GMT  
		Size: 197.4 MB (197415907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a450ebe0d82d5db4ad899d4f2a53050053fac218d7840792c212150656906d9b`  
		Last Modified: Tue, 12 Dec 2023 20:23:07 GMT  
		Size: 3.8 MB (3833969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:574f36bbcd459076f74f761030f07f61856a72dbd75ae319db1816041682b69b`  
		Last Modified: Tue, 12 Dec 2023 20:23:06 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
