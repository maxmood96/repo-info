## `eclipse-temurin:17-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:c42b84196616e4427446f4997117086f275ee0155f05e12a9038febe8f1156fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6054; amd64

### `eclipse-temurin:17-jre-nanoserver-1809` - windows version 10.0.17763.6054; amd64

```console
$ docker pull eclipse-temurin@sha256:6f041482e741ec97682b12af46d7322f4c32e3b6fa6d63ad1d356dfebb75d8c5
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.6 MB (201589775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65a360800507fa6e894933046047aec8a6977a6238fa55ad2229deddb500d500`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 03 Jul 2024 00:02:58 GMT
RUN Apply image 10.0.17763.6054
# Wed, 10 Jul 2024 16:38:43 GMT
SHELL [cmd /s /c]
# Wed, 10 Jul 2024 16:54:52 GMT
ENV JAVA_VERSION=jdk-17.0.11+9
# Wed, 10 Jul 2024 16:54:53 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 10 Jul 2024 16:54:53 GMT
USER ContainerAdministrator
# Wed, 10 Jul 2024 16:54:59 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 10 Jul 2024 16:55:00 GMT
USER ContainerUser
# Wed, 10 Jul 2024 16:59:11 GMT
COPY dir:a78f43753c24e3e0717a998b116850ca8c6149210b4cd2529d3fd312f361a7bd in C:\openjdk-17 
# Wed, 10 Jul 2024 16:59:20 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:53308e1345e8a502fe824770c132f9d645d42108fee87a0708ea8814c901e40d`  
		Last Modified: Tue, 09 Jul 2024 17:42:24 GMT  
		Size: 155.1 MB (155081383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c00a79547db1bc3ab4a5550f2ec9ba165e302f4a4984af3c1bfbbbe1726a3bf6`  
		Last Modified: Wed, 10 Jul 2024 17:28:00 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa6fc257700c11bed092d5f4a760daaab80965764eb09f2283dedb1d0e4760d8`  
		Last Modified: Wed, 10 Jul 2024 17:32:44 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22c7f318c2d77b6c252f873c0df5a1b45c9d1bdef19335413511d13b35e6e818`  
		Last Modified: Wed, 10 Jul 2024 17:32:44 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1eeb5e48c49f4874272e8484351900a3776ee98fb23b8e08c36b7c089363acc`  
		Last Modified: Wed, 10 Jul 2024 17:32:44 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af1cf98a81ae29a347fd16ce89d3a53f0879bb16b045a5027e7eead282d545f5`  
		Last Modified: Wed, 10 Jul 2024 17:32:42 GMT  
		Size: 68.9 KB (68852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed0e48837678870a6f7b286282e6251555e5f188e2d56bc47103872dd2efbc79`  
		Last Modified: Wed, 10 Jul 2024 17:32:42 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b469cd0bb32d673bb05621c99cddaa693d374effec6cb4b058f14bf797016552`  
		Last Modified: Wed, 10 Jul 2024 17:33:49 GMT  
		Size: 43.5 MB (43453995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a52007d0bdc40e5bc5e2e5ecd21b82b906881b427bd48cc6a28555897764df`  
		Last Modified: Wed, 10 Jul 2024 17:33:42 GMT  
		Size: 3.0 MB (2979767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
