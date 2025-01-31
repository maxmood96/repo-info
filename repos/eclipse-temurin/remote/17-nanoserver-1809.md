## `eclipse-temurin:17-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:a1595dbf31c912c275911dd25aa253756fb650b104f722fd7fc153958e6cbaa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `eclipse-temurin:17-nanoserver-1809` - windows version 10.0.17763.6775; amd64

```console
$ docker pull eclipse-temurin@sha256:b7b47b197eae9d0f5c5cf667a8e904860c938ed307c222fc2afa1cdfb5143bae
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.2 MB (346169609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b0fd78ea5df401a9b57b0ffe532d3d5f83010afae89dbe2c1a478ef4303e648`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 09 Jan 2025 09:30:10 GMT
RUN Apply image 10.0.17763.6775
# Fri, 31 Jan 2025 02:11:58 GMT
SHELL [cmd /s /c]
# Fri, 31 Jan 2025 02:12:01 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Fri, 31 Jan 2025 02:12:01 GMT
ENV JAVA_HOME=C:\openjdk-17
# Fri, 31 Jan 2025 02:12:02 GMT
USER ContainerAdministrator
# Fri, 31 Jan 2025 02:12:24 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 31 Jan 2025 02:12:24 GMT
USER ContainerUser
# Fri, 31 Jan 2025 02:12:38 GMT
COPY dir:5f87ec570fea10148b246e6a91d6cf8396b47b1e19a7e8d79bcea78e84a1d159 in C:\openjdk-17 
# Fri, 31 Jan 2025 02:12:44 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 31 Jan 2025 02:12:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3a71a517ad886518458023f01614036e271bdcdb366b9c2c64b1b5dd7737a6b0`  
		Last Modified: Tue, 14 Jan 2025 20:45:12 GMT  
		Size: 155.3 MB (155267564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e78da691f2e8b831bd700d6ae60c934b4cb355e1893aa4beda1e7383ff08546`  
		Last Modified: Fri, 31 Jan 2025 02:12:51 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c342b4e35600436faa76075739d5f846bf3754447236c9e120b49a9fb517c8d`  
		Last Modified: Fri, 31 Jan 2025 02:12:51 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:437590683fedcb758d27eeb7a565b37e10fc3759881fea9784fc8c3beb9c49e2`  
		Last Modified: Fri, 31 Jan 2025 02:12:51 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e19b665ee24b092c2031357310fd0d266deed4daa26033af403a402e7ca928f`  
		Last Modified: Fri, 31 Jan 2025 02:12:50 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130ce49924a644188e6348597f69520bee740cc0d0931043375ca945dd2e8a08`  
		Last Modified: Fri, 31 Jan 2025 02:12:49 GMT  
		Size: 66.0 KB (66043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0303361c4a0b1687f7c1c02a0b207b9e7fec76a3af9075095cdae1648edd31f`  
		Last Modified: Fri, 31 Jan 2025 02:12:49 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc746e2ec3ffdbff0e2b5e1fa88a61b16cb72badc33d983ff062c4912af6df4b`  
		Last Modified: Fri, 31 Jan 2025 02:12:58 GMT  
		Size: 187.2 MB (187234424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7d1395adc954ae2d0c21f57de7a9a14cb1e3d0ce858235e48a03bda6f05d255`  
		Last Modified: Fri, 31 Jan 2025 02:12:49 GMT  
		Size: 3.6 MB (3595350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ab652f5aa3a0d6e390de2f00b257bcd569748eaf181fc2437a877d1eb2a473b`  
		Last Modified: Fri, 31 Jan 2025 02:12:49 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
