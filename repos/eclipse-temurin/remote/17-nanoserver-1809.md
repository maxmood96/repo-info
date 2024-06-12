## `eclipse-temurin:17-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:148750b8ac3cab4ab7612542ff55e0b57eac89f9c8cdde88bc9043ce3bb53545
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5936; amd64

### `eclipse-temurin:17-nanoserver-1809` - windows version 10.0.17763.5936; amd64

```console
$ docker pull eclipse-temurin@sha256:1bc49f2ba2fedfb58066f1f87e2e120f2fd23e8bef4237a2416cd7a0676ce011
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.6 MB (345558830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cd6a01d39502413f2c2b1d705467d462fac8736f74df0c1f666a805af44ce88`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Jun 2024 10:54:05 GMT
RUN Apply image 10.0.17763.5936
# Wed, 12 Jun 2024 17:41:08 GMT
SHELL [cmd /s /c]
# Wed, 12 Jun 2024 18:01:17 GMT
ENV JAVA_VERSION=jdk-17.0.11+9
# Wed, 12 Jun 2024 18:01:17 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 12 Jun 2024 18:01:18 GMT
USER ContainerAdministrator
# Wed, 12 Jun 2024 18:01:26 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 12 Jun 2024 18:01:27 GMT
USER ContainerUser
# Wed, 12 Jun 2024 18:01:41 GMT
COPY dir:58180deb8c422e61d331dbc12d9d7d83d7afe3e9097adb59bd0860aff4211c36 in C:\openjdk-17 
# Wed, 12 Jun 2024 18:01:53 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 12 Jun 2024 18:01:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4f703ea968d7f7434cf61e5d835cb3c507a6364ff8c7b3b96b73391b22115615`  
		Last Modified: Tue, 11 Jun 2024 20:35:02 GMT  
		Size: 155.0 MB (155033193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce076c01ab33a997d8fa4a6a49752f31455fef6df331991ad3b3736b3567321`  
		Last Modified: Wed, 12 Jun 2024 18:40:43 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ef4283eaec67ab82eb2eaf1394d348ef4b8095aae26938603564e9753ed3dd7`  
		Last Modified: Wed, 12 Jun 2024 18:46:00 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0971dcb75451d4945808f751c16bd6b1107708957392106f500273c3cf43c75`  
		Last Modified: Wed, 12 Jun 2024 18:45:59 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a3fca7aa45609ebcb6f1aa65ba03489b6c380371840a7fc5a632bcd0ac82392`  
		Last Modified: Wed, 12 Jun 2024 18:45:59 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cba8307dff66a644bbf0fc5a0ff9fade24aa29f5e1cb3bffbacb7750b6cad920`  
		Last Modified: Wed, 12 Jun 2024 18:45:57 GMT  
		Size: 69.0 KB (69006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfc382ff7ccb019cad431b62ae9298ebe9978a095189f90effbaad82ad26c18b`  
		Last Modified: Wed, 12 Jun 2024 18:45:57 GMT  
		Size: 1.1 KB (1117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee897e1a071b3afd6ae08b496852edc6ba1d0f4435ad9a4d0b5db4d1eec72ede`  
		Last Modified: Wed, 12 Jun 2024 18:46:15 GMT  
		Size: 186.8 MB (186837675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0155fe02bdeed1b382320fc46f20130f5d5f31384969519752fa2e8465b7b92`  
		Last Modified: Wed, 12 Jun 2024 18:45:58 GMT  
		Size: 3.6 MB (3611978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2899c8a81b879525f1137bccf3723ac4149b3d00d893a8088e7152a4fc25c6f9`  
		Last Modified: Wed, 12 Jun 2024 18:45:57 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
