## `eclipse-temurin:17-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:452159176966a6171140bb897c84a82d0ac5b18ad0a3a19dc4ba45222d01e12d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `eclipse-temurin:17-jre-nanoserver-1809` - windows version 10.0.17763.7009; amd64

```console
$ docker pull eclipse-temurin@sha256:066d150620296d22268d58337502b9bce72126669accb7ba8f0e7486aee812d3
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.7 MB (153702357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a8f30bd7f21d529c4b30f9b81b6f659370327be7747ea8eca4168e4e46c7c2c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 05 Mar 2025 21:54:26 GMT
RUN Apply image 10.0.17763.7009
# Wed, 12 Mar 2025 19:21:51 GMT
SHELL [cmd /s /c]
# Wed, 12 Mar 2025 19:21:52 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Wed, 12 Mar 2025 19:21:53 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 12 Mar 2025 19:21:53 GMT
USER ContainerAdministrator
# Wed, 12 Mar 2025 19:21:56 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 12 Mar 2025 19:21:56 GMT
USER ContainerUser
# Wed, 12 Mar 2025 19:22:01 GMT
COPY dir:e48212bf4bd9a001a558a3ce6925b9b3b6903c8af46347cbb9e06ca86192ff86 in C:\openjdk-17 
# Wed, 12 Mar 2025 19:22:05 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:543388a101bf4d470af7e8817eff3f6f3b98f13d106939ab3f507a28f2825d0a`  
		Last Modified: Tue, 11 Mar 2025 22:40:48 GMT  
		Size: 106.9 MB (106907688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fbcdb05d17a35d4540cbff011027f76dd304c4a4f7ae4cf919ce03d2dbab5e4`  
		Last Modified: Wed, 12 Mar 2025 19:22:12 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6491a02174ed611b5c08cd5a6ca10faa8b95227abd0a08473bfffb6d9625a0d`  
		Last Modified: Wed, 12 Mar 2025 19:22:12 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec08622e8b2702c55ce643f805c84177d5601662f920f7f0aefa480f76530e0c`  
		Last Modified: Wed, 12 Mar 2025 19:22:12 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64645226d162a4c87d2c83a020973b457806b181bf6c7a127a6ff1bd51316943`  
		Last Modified: Wed, 12 Mar 2025 19:22:10 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55b95865f475adf72dad2d6be1118c2a95efcca04c380c00d7ab6b6eaf8a584`  
		Last Modified: Wed, 12 Mar 2025 19:22:10 GMT  
		Size: 69.1 KB (69057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5c2c687d6057e406e00ce86aa72858009eea06ee10871616156f8f0d3aa29a7`  
		Last Modified: Wed, 12 Mar 2025 19:22:10 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d563e27763c6606c000230a4040628104ca097daed128c354be956924b51cbc`  
		Last Modified: Wed, 12 Mar 2025 19:22:15 GMT  
		Size: 43.7 MB (43727211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88592db5e555a15d8d87f3982b54c4ee07afa3ca7ae106900ba914368e2cfb44`  
		Last Modified: Wed, 12 Mar 2025 19:22:11 GMT  
		Size: 3.0 MB (2993204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
