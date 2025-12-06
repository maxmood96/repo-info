## `openjdk:27-ea-1-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:bef73a71cff96c9f85cb9ee94328eff18ef7e75cdf0464cd94dac56d268cc479
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `openjdk:27-ea-1-nanoserver-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull openjdk@sha256:41de23e6faf6d987a0e9ce7a833dfe742a7588458b23fdb12881caff78176740
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.8 MB (351788673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f9aa0834386fce181fa7edb3ef36df895dca96e29f8b831a09254e56c97072d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 05 Nov 2025 05:29:25 GMT
RUN Apply image 10.0.20348.4405
# Sat, 06 Dec 2025 01:13:27 GMT
SHELL [cmd /s /c]
# Sat, 06 Dec 2025 01:13:30 GMT
ENV JAVA_HOME=C:\openjdk-27
# Sat, 06 Dec 2025 01:13:31 GMT
USER ContainerAdministrator
# Sat, 06 Dec 2025 01:13:43 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Sat, 06 Dec 2025 01:13:43 GMT
USER ContainerUser
# Sat, 06 Dec 2025 01:13:44 GMT
ENV JAVA_VERSION=27-ea+1
# Sat, 06 Dec 2025 01:15:01 GMT
COPY dir:19d14afdca91419101de212977382a6561545d70f03a447b9d85c65ba4bb2f53 in C:\openjdk-27 
# Sat, 06 Dec 2025 01:15:14 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Sat, 06 Dec 2025 01:15:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f1a2bf860779d298b0b94004e0d2d04a95d761e823b0c7184234535c0d000ef5`  
		Last Modified: Tue, 11 Nov 2025 19:13:45 GMT  
		Size: 126.3 MB (126349074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14cc323382920c4c1c3ce301ebf7acfc3be7339553a6e78fcf51ded00c29cd0`  
		Last Modified: Sat, 06 Dec 2025 01:15:45 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c58798ab577651ab2199beee182df10bff3ff178116b412783c614c55beb1fbe`  
		Last Modified: Sat, 06 Dec 2025 01:15:45 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b28b3216e572afce48a9af2cc1d4c8e8c031bac4d4fcd186284f780a5587423b`  
		Last Modified: Sat, 06 Dec 2025 01:15:46 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fdfbdae664ead4c617ddeccca64bb938b3851dbfe309587f6dec77cf19a42c2`  
		Last Modified: Sat, 06 Dec 2025 01:15:46 GMT  
		Size: 83.0 KB (83006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a398bcc13d2deb0d74dae5cdac82e38c8727bfc45f4244855e21ce24ed167185`  
		Last Modified: Sat, 06 Dec 2025 01:15:46 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6261378a7384dc1e548b2138ae5dccc9a01da2d9091fd83a06d62db84854149`  
		Last Modified: Sat, 06 Dec 2025 01:15:46 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:303fc0538eada97438327deec562098e2d51b4e0c3507c79ca4a41a22ba8471d`  
		Last Modified: Sat, 06 Dec 2025 01:16:01 GMT  
		Size: 225.2 MB (225224798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:916e63873a8ef5e84d8b6c41ce5c6eea8a6f71d912231a144a64c8d62de19118`  
		Last Modified: Sat, 06 Dec 2025 01:15:46 GMT  
		Size: 125.5 KB (125489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:285d14cd3ec8bfd9dc63dfa66821af3f76e82a6ed9eb191df2de559b83dcd66c`  
		Last Modified: Sat, 06 Dec 2025 01:15:46 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
