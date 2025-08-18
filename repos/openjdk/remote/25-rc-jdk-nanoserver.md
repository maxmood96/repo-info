## `openjdk:25-rc-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:cef9ee798eb0bc929be149a85631a41f90b56d659ac61fb8feac41564564f89e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4946; amd64
	-	windows version 10.0.20348.4052; amd64

### `openjdk:25-rc-jdk-nanoserver` - windows version 10.0.26100.4946; amd64

```console
$ docker pull openjdk@sha256:4ba9345c07f8988a96dbfe8768b3fd2d127e8e29095221132b2340473e6871a1
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **412.2 MB (412217730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b7a3a18b1f6ba4607314c190a2962f473401403895a2e5cf7bda842dc71e579`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 10 Aug 2025 02:44:20 GMT
RUN Apply image 10.0.26100.4946
# Mon, 18 Aug 2025 19:13:05 GMT
SHELL [cmd /s /c]
# Mon, 18 Aug 2025 19:13:05 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 18 Aug 2025 19:13:05 GMT
USER ContainerAdministrator
# Mon, 18 Aug 2025 19:13:07 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 18 Aug 2025 19:13:08 GMT
USER ContainerUser
# Mon, 18 Aug 2025 19:13:08 GMT
ENV JAVA_VERSION=25
# Mon, 18 Aug 2025 19:13:14 GMT
COPY dir:72a77cd8dd8fd9224e7c68e3876c18f0a900359f2fadd93c9163ab7d4997de07 in C:\openjdk-25 
# Mon, 18 Aug 2025 19:13:17 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 18 Aug 2025 19:13:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6d63d98dae9e3419e8c965c24a11d30e40947cf35ee17c204c5d8b7bae7ff2ef`  
		Last Modified: Tue, 12 Aug 2025 21:13:38 GMT  
		Size: 193.5 MB (193469373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0221ac58abc503b742be752747e7b01ff3069fcc200826abf3d5ec4e827dceac`  
		Last Modified: Mon, 18 Aug 2025 19:14:01 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:367d824426a232d61f2fcbcf139f8be28c638bbb1ea80ad4cdf677ccf52238d5`  
		Last Modified: Mon, 18 Aug 2025 19:14:02 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f60a130b0ea86e2a4a9743c3a926274961e171890f3293970977c52ed3261c41`  
		Last Modified: Mon, 18 Aug 2025 19:14:01 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f10efc14e4d466d196473f0cae1610033d9e2e52e94e4b08a0dad16dc6fed988`  
		Last Modified: Mon, 18 Aug 2025 19:14:03 GMT  
		Size: 75.7 KB (75679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fe307594353a94e2658232447ff4d9236cd8538f22e394d0c72491723ce3c44`  
		Last Modified: Mon, 18 Aug 2025 19:14:02 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d31f6cf2e305acfab2e2cf24299f6e0fcc1e2a5155c0e1063011e01fefaa3618`  
		Last Modified: Mon, 18 Aug 2025 19:14:04 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f5f5b5d6bc1ed90f1d449c4d7e94a7f0f7cdbd1e872849dc19aa33f447d3d9e`  
		Last Modified: Mon, 18 Aug 2025 21:24:03 GMT  
		Size: 218.6 MB (218553034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d3f747e5a2f4f2df6eacb6e62ffa1ca487a7c2f0eeb22002e3979917b4ec824`  
		Last Modified: Mon, 18 Aug 2025 19:14:05 GMT  
		Size: 113.4 KB (113356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6c5d0e50e7149bac07d4c3bf9e981dd95e306aca43d2721c4608932d1c3687c`  
		Last Modified: Mon, 18 Aug 2025 19:14:05 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:25-rc-jdk-nanoserver` - windows version 10.0.20348.4052; amd64

```console
$ docker pull openjdk@sha256:b7ec10d826367664f2c6a3df691fc47f32ce5871e717d35e5a500814c0655348
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.4 MB (341403653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0aa6ffdc71b76a2441b2cf1970c45fb2ad141dd621b68c83d0a820428ce40d0`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Mon, 18 Aug 2025 19:13:20 GMT
SHELL [cmd /s /c]
# Mon, 18 Aug 2025 19:13:21 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 18 Aug 2025 19:13:22 GMT
USER ContainerAdministrator
# Mon, 18 Aug 2025 19:13:26 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 18 Aug 2025 19:13:27 GMT
USER ContainerUser
# Mon, 18 Aug 2025 19:13:28 GMT
ENV JAVA_VERSION=25
# Mon, 18 Aug 2025 19:13:38 GMT
COPY dir:72a77cd8dd8fd9224e7c68e3876c18f0a900359f2fadd93c9163ab7d4997de07 in C:\openjdk-25 
# Mon, 18 Aug 2025 19:13:44 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 18 Aug 2025 19:13:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:798af82ed8f76ac9848825076ef8adbfb0df401322321804c8d8319fbe1eb2d2`  
		Last Modified: Mon, 18 Aug 2025 19:22:07 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e23e571f59eee2cc6e2ad5a318d5b10a92613d91b27a75672ab61d7d25ca0d7`  
		Last Modified: Mon, 18 Aug 2025 19:22:10 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b42f1a8d91780568c88bb4614dacc85aa26cc02bb363f25d309c109282f4e1dc`  
		Last Modified: Mon, 18 Aug 2025 19:22:14 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad9a5116ef0465043d9de6c01017a57a16ceac4cf2e86689ae26cbf1e9e409a5`  
		Last Modified: Mon, 18 Aug 2025 19:22:18 GMT  
		Size: 78.2 KB (78159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd242ef13a69499200634b2e284f31534ef620cbd56d4d952ef7011b3fd8611a`  
		Last Modified: Mon, 18 Aug 2025 19:22:23 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db610df64aa60c9dd872e1ebfea29ed963322439f5cc66532fa876d7c6999ee9`  
		Last Modified: Mon, 18 Aug 2025 19:22:26 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:615ae9b3837f0abe566f7d7e1076f181f676116b3d1e594db70dcc8efeb29a95`  
		Last Modified: Mon, 18 Aug 2025 21:24:17 GMT  
		Size: 218.6 MB (218551925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41eb15e174dce2e3096be026927612296f43085caae37fc4f61ba1392944fc6`  
		Last Modified: Mon, 18 Aug 2025 19:22:31 GMT  
		Size: 107.0 KB (107020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb8b26d7517dcea271f9fb7012323d74fc06f3bed4b193bb12960af6e175939a`  
		Last Modified: Mon, 18 Aug 2025 19:22:34 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
