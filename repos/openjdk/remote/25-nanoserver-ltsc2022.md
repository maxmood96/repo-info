## `openjdk:25-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:ed0e8ed6989454f826882fbc5099fb9c85523c344668415a66f7ca09c27f7ac0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3328; amd64

### `openjdk:25-nanoserver-ltsc2022` - windows version 10.0.20348.3328; amd64

```console
$ docker pull openjdk@sha256:332117e23363b6d7be48e35f79848aedaf23d8e8658efade088f80bbd074571a
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.3 MB (328271277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8aefde0ab5d11ad4ebb2d276e94d2186b87452361be593c1b3c5a97fcff0076`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 06 Mar 2025 10:30:39 GMT
RUN Apply image 10.0.20348.3328
# Wed, 12 Mar 2025 19:22:18 GMT
SHELL [cmd /s /c]
# Wed, 12 Mar 2025 19:22:19 GMT
ENV JAVA_HOME=C:\openjdk-25
# Wed, 12 Mar 2025 19:22:20 GMT
USER ContainerAdministrator
# Wed, 12 Mar 2025 19:22:24 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 12 Mar 2025 19:22:25 GMT
USER ContainerUser
# Wed, 12 Mar 2025 19:22:26 GMT
ENV JAVA_VERSION=25-ea+13
# Wed, 12 Mar 2025 19:22:34 GMT
COPY dir:41adcea28f6e8239eac0b74c19049c5daef67ad138ba9db7bdf8df0acc8b0b9b in C:\openjdk-25 
# Wed, 12 Mar 2025 19:22:39 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 12 Mar 2025 19:22:40 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:47ec0d45ee7716f773dfebb62d84eb3893d3af9baf9c799960566b016a17e330`  
		Last Modified: Wed, 12 Mar 2025 02:22:56 GMT  
		Size: 120.7 MB (120695547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c2f17cecf881f104c1c9863a9939b7951a727238e9cef089c188c26320657e`  
		Last Modified: Wed, 12 Mar 2025 19:22:45 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2b8fb0c1c384a3635a96c4b7a79c57756b8aae9b195babdd37119f42546be93`  
		Last Modified: Wed, 12 Mar 2025 19:22:46 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92a61f49c35186bcd6dff87df3755ae19e196edab80d5bca0bcaa480bcf89d37`  
		Last Modified: Wed, 12 Mar 2025 19:22:45 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a318be4c4c064770438b69f3fa62d2976e9310545b4d7d25fecbc2f4732efbe2`  
		Last Modified: Wed, 12 Mar 2025 19:22:45 GMT  
		Size: 73.1 KB (73086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43ac77ec3f311bdb46c1a4311ff49f2565283440164928d92446078689dd2eb3`  
		Last Modified: Wed, 12 Mar 2025 19:22:43 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ab50dc0c2d10d2bc209422267bd346fc140120ed38ca35f29337b5807bc816c`  
		Last Modified: Wed, 12 Mar 2025 19:22:43 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80281f30648e178a66ef27279490823213c3551a501e687fe01774c862359569`  
		Last Modified: Wed, 12 Mar 2025 19:22:55 GMT  
		Size: 207.4 MB (207398992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d87243abdb80a42b54ea68cf29209463726ceac287ca9af6be95abb3afe7f6c3`  
		Last Modified: Wed, 12 Mar 2025 19:22:43 GMT  
		Size: 97.3 KB (97341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2109cac3a05aeec383a0b1af8dbb1611a97772a09c0540651876a346deb010e`  
		Last Modified: Wed, 12 Mar 2025 19:22:43 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
