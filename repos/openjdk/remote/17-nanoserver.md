## `openjdk:17-nanoserver`

```console
$ docker pull openjdk@sha256:9ae5ab4c1193cf59671952f56c0cd10d5522571f5f5822c5141d11efcf1d9920
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1697; amd64

### `openjdk:17-nanoserver` - windows version 10.0.17763.1697; amd64

```console
$ docker pull openjdk@sha256:27afba75da2c17151a430ee0fb74dddbd60c130be25f554352489a9f5f6adfbf
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.0 MB (286049547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:884d54245fc25a9dc06fa9e21ef347ec59ce63cde50574ef26bac1a49719a554`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 07 Jan 2021 16:14:35 GMT
RUN Apply image 1809-amd64
# Wed, 13 Jan 2021 19:56:48 GMT
SHELL [cmd /s /c]
# Wed, 13 Jan 2021 19:56:48 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 13 Jan 2021 19:56:49 GMT
USER ContainerAdministrator
# Mon, 01 Feb 2021 19:22:27 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 01 Feb 2021 19:22:28 GMT
USER ContainerUser
# Mon, 01 Feb 2021 19:22:28 GMT
ENV JAVA_VERSION=17-ea+7
# Mon, 01 Feb 2021 19:22:41 GMT
COPY dir:ad6280aea1790406d8f9c52ebfea42e20f75f1cf88a6b84ca634d20fa70351ca in C:\openjdk-17 
# Mon, 01 Feb 2021 19:22:52 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 01 Feb 2021 19:22:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:62239e9aa1a352a20b0d4969c2b508b8a18d10e799d4db72e6f24ccbb2c724d9`  
		Size: 101.3 MB (101340070 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c2b6c001c337f812bceb3b03d15a70d1d9905540658e751e42f20f7cc0ddc819`  
		Last Modified: Wed, 13 Jan 2021 21:16:47 GMT  
		Size: 908.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:788a0bd344d2eb3850ddd4570305cbcf959de9a743a310f941c297081c240d8f`  
		Last Modified: Wed, 13 Jan 2021 21:16:46 GMT  
		Size: 869.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6db311194c9cbd0c67151ee177949a18a7ad83e5551b659b30ef3151062c5a98`  
		Last Modified: Wed, 13 Jan 2021 21:16:47 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6df1939641b7f54cacd46e02c3a2331df7de05527860cba622a289f0c5e195c7`  
		Last Modified: Mon, 01 Feb 2021 19:57:33 GMT  
		Size: 68.4 KB (68408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2725371e5f3ecc54b6264bcd3123ec0bd036d480a3110dba6761e7999496c08c`  
		Last Modified: Mon, 01 Feb 2021 19:57:30 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33537d95e13c279bcce787c54e1a1ec45c7cc862b6a519243c8151ab0727375d`  
		Last Modified: Mon, 01 Feb 2021 19:57:30 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c0137cd0b971479491b5480d2f59e2de34b49a1026d9b8e94da875a3501047f`  
		Last Modified: Mon, 01 Feb 2021 19:57:49 GMT  
		Size: 181.0 MB (180990018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bd87184aaf556c6299828493cd4ba080611e400096c9025cafd7a52ea735ea9`  
		Last Modified: Mon, 01 Feb 2021 19:57:34 GMT  
		Size: 3.6 MB (3645089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b925c815b62ecb2247806d93afcaec30835d7c76f2e79264554fd25732b7718`  
		Last Modified: Mon, 01 Feb 2021 19:57:30 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
