## `openjdk:27-ea-1-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:1579bd69aec72b4cbebe7c65b0c67a02de9d9a984e4c0e292eb0634975bd0e04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.7171; amd64
	-	windows version 10.0.20348.4405; amd64

### `openjdk:27-ea-1-jdk-nanoserver` - windows version 10.0.26100.7171; amd64

```console
$ docker pull openjdk@sha256:cdbfae6c4bd0b56d4973815e5511d241b6ef4118ce257f5e2ae220066ba9c4aa
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **423.4 MB (423366563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8117e50987e4ff523f8acf8dca915b474d730215db2d687cc38f51d796c18136`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 09 Nov 2025 10:04:50 GMT
RUN Apply image 10.0.26100.7171
# Sat, 06 Dec 2025 01:10:55 GMT
SHELL [cmd /s /c]
# Sat, 06 Dec 2025 01:10:55 GMT
ENV JAVA_HOME=C:\openjdk-27
# Sat, 06 Dec 2025 01:10:56 GMT
USER ContainerAdministrator
# Sat, 06 Dec 2025 01:11:01 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Sat, 06 Dec 2025 01:11:02 GMT
USER ContainerUser
# Sat, 06 Dec 2025 01:11:02 GMT
ENV JAVA_VERSION=27-ea+1
# Sat, 06 Dec 2025 01:11:26 GMT
COPY dir:19d14afdca91419101de212977382a6561545d70f03a447b9d85c65ba4bb2f53 in C:\openjdk-27 
# Sat, 06 Dec 2025 01:11:32 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Sat, 06 Dec 2025 01:11:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:87c91227213eb6e7c8cfe33b6bd0429350e524756878f37f3860b013f804bf59`  
		Last Modified: Tue, 11 Nov 2025 20:41:49 GMT  
		Size: 197.9 MB (197936447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a34b994c3a0baca4a33590c55ad71fd48c8bd33fc51590f0c85bbf73b0a6673d`  
		Last Modified: Sat, 06 Dec 2025 01:12:01 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36ce0ae84b908c6a0cfe8aafcf339909f42aa382f1705df492e5781a7801a0dc`  
		Last Modified: Sat, 06 Dec 2025 01:12:01 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62e187b97a1922ce55e5b59f0fec161e7cb080aed5b6ff54b386dd0f92afddce`  
		Last Modified: Sat, 06 Dec 2025 01:12:01 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cae13ac734d53aec6a690389cbdfda422589cf9650be215f03b91260111330f`  
		Last Modified: Sat, 06 Dec 2025 01:12:01 GMT  
		Size: 75.4 KB (75448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca224a56cee254e02886c8e368295e687dec13c11597f5ac45b12b4a507f4f16`  
		Last Modified: Sat, 06 Dec 2025 01:12:01 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2e485bf4ac9fd8a1006e3219e8d886f7c64d74c2a55d128a7a93ce28cc49d96`  
		Last Modified: Sat, 06 Dec 2025 01:12:02 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5181075a90965ff92a19a177f6fac6f7aa8e0005e2c6e4cd02de416540b7178`  
		Last Modified: Sat, 06 Dec 2025 01:13:11 GMT  
		Size: 225.2 MB (225224756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edf313a93185b45bece000dc662f7599703a136a602c34c717df922358755c7f`  
		Last Modified: Sat, 06 Dec 2025 01:12:02 GMT  
		Size: 123.5 KB (123548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a6b7b2a4abce7e879e9794937f93341453e5e0903d0837148f55b4ffbda5b81`  
		Last Modified: Sat, 06 Dec 2025 01:12:02 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:27-ea-1-jdk-nanoserver` - windows version 10.0.20348.4405; amd64

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
