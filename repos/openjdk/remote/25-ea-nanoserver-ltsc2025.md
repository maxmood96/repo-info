## `openjdk:25-ea-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:4e96cf4eb332bf936495e8434aab0190dd83378efedd67648ce99de2c803d291
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4652; amd64

### `openjdk:25-ea-nanoserver-ltsc2025` - windows version 10.0.26100.4652; amd64

```console
$ docker pull openjdk@sha256:94826f9f31cbcc28805c1d02d2cfafeb6e8c907fef7b4eecfea17afe63e4a3ef
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **411.9 MB (411877553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a443faead9ba69fa27023668d3d53d392ad7d906e24ee93fc517fd8c03bf352`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 05 Jul 2025 18:13:07 GMT
RUN Apply image 10.0.26100.4652
# Wed, 09 Jul 2025 19:15:06 GMT
SHELL [cmd /s /c]
# Wed, 09 Jul 2025 19:15:07 GMT
ENV JAVA_HOME=C:\openjdk-25
# Wed, 09 Jul 2025 19:15:08 GMT
USER ContainerAdministrator
# Wed, 09 Jul 2025 19:15:12 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 09 Jul 2025 19:15:13 GMT
USER ContainerUser
# Wed, 09 Jul 2025 19:15:15 GMT
ENV JAVA_VERSION=25-ea+30
# Wed, 09 Jul 2025 19:15:23 GMT
COPY dir:3f4870c1d66808f40120812f97095242c2c5faef4fbe09ec60976bc998095719 in C:\openjdk-25 
# Wed, 09 Jul 2025 19:15:32 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 09 Jul 2025 19:15:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2fd4507679915420227c89c4f57165747b37deaa62748936e2af8c2f38de0b4e`  
		Last Modified: Wed, 09 Jul 2025 01:51:41 GMT  
		Size: 193.2 MB (193150329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6a9b8b667061f67e9247d678ded0b6141bfb860e15277def1155385c56df44c`  
		Last Modified: Wed, 09 Jul 2025 19:16:02 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:236d28e84c24e3ea566f2f145bbe7c591d525a7a12e800191d5a4e96bfa87b84`  
		Last Modified: Wed, 09 Jul 2025 19:16:02 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e86ebd0b2d31386111d740db207514b9138d6057e13ad343aeb88285afe0f8e6`  
		Last Modified: Wed, 09 Jul 2025 19:16:02 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:914162515321c78ffb3fb189e57cc52c15d98626272e39869cbb6b60255b29a9`  
		Last Modified: Wed, 09 Jul 2025 19:16:02 GMT  
		Size: 76.5 KB (76483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f957af8ec6d7fe07078aab1f6915a3d181fa491ef657d3de13541eee20d0473`  
		Last Modified: Wed, 09 Jul 2025 19:16:02 GMT  
		Size: 1.1 KB (1095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f01fde13232f2ae8f191018f8a35678e00412bba83fc4538fe315d37de5ea67`  
		Last Modified: Wed, 09 Jul 2025 19:16:02 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef02fcf2235582464b643306e83c111267dcfbd7d3ac2c52f548e0d2002b789a`  
		Last Modified: Wed, 09 Jul 2025 21:23:50 GMT  
		Size: 218.5 MB (218529771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0087087e4abe07f3dd88c5d5e226452f2e67e9f1aea78f6069f071105082e717`  
		Last Modified: Wed, 09 Jul 2025 19:16:02 GMT  
		Size: 114.6 KB (114598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a9d6e3e636d85f17c0f593a8ce0589b127f249bf87889c6dd3bc002e591183c`  
		Last Modified: Wed, 09 Jul 2025 19:16:02 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
