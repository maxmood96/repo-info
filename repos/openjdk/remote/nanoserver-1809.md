## `openjdk:nanoserver-1809`

```console
$ docker pull openjdk@sha256:c52d50ef8001b9a5c867a1e8a339f1a366a7952977f128c1ba9751f07b6b5f59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2061; amd64

### `openjdk:nanoserver-1809` - windows version 10.0.17763.2061; amd64

```console
$ docker pull openjdk@sha256:be29dfea4463b5d43f896ce216bb81e5d26acd9c65251cafddd1c39f36e243df
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.5 MB (286545349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:146c8940ad857727b6060372b765fbff70d9dc1f8a07ede6f2c7d4cc393a13f7`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 06 Jul 2021 20:06:39 GMT
RUN Apply image 1809-amd64
# Wed, 14 Jul 2021 02:53:30 GMT
SHELL [cmd /s /c]
# Wed, 14 Jul 2021 03:10:50 GMT
ENV JAVA_HOME=C:\openjdk-16
# Wed, 14 Jul 2021 03:10:53 GMT
USER ContainerAdministrator
# Wed, 14 Jul 2021 03:11:07 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 14 Jul 2021 03:11:10 GMT
USER ContainerUser
# Wed, 21 Jul 2021 00:21:02 GMT
ENV JAVA_VERSION=16.0.2
# Wed, 21 Jul 2021 00:21:19 GMT
COPY dir:cb0fff7e1eb7273b9cd408e88cd60c60a3923c3595eb85b84f5ecaf2afd41761 in C:\openjdk-16 
# Wed, 21 Jul 2021 00:21:47 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 21 Jul 2021 00:21:49 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:29d43e56445c5279a6386c4dfe4d1ada3c7124ade9cb7b0f2757e58ffc7cd10b`  
		Size: 102.7 MB (102725622 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:78d8754fb12dd351c91bed29d92c703cddb135a78d8f056b6a3bf13a251c1d2d`  
		Last Modified: Wed, 14 Jul 2021 03:42:27 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdf9694a21ba555df087e8739998eca9a0b56540365a4cba596a87fa3e2c41ea`  
		Last Modified: Wed, 14 Jul 2021 03:53:04 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3911007b3fc33a0faac9b39ed10a6ae256b02f1e7c47048c129b6ad09d99ca2`  
		Last Modified: Wed, 14 Jul 2021 03:53:04 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fce5e7db34dd013fa3d55087c8194334bd63cfd45e4466e0d55b55f63ce9398e`  
		Last Modified: Wed, 14 Jul 2021 03:53:04 GMT  
		Size: 65.0 KB (65038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89bbdb6526137bb3e66d6e831498bd6a0a30d786ebc3980ad9ded3e8b3eee0d5`  
		Last Modified: Wed, 14 Jul 2021 03:53:01 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7898d9169494ebad7d2cb9f673ebec018284c81d2f23fefd8c1c72261e2ae45f`  
		Last Modified: Wed, 21 Jul 2021 00:31:22 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:762536276b96006d8ee5ec00c3b6720d2708997f4209c0fab6fe465077781e1b`  
		Last Modified: Wed, 21 Jul 2021 00:34:54 GMT  
		Size: 180.1 MB (180093206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7d9249b6c0e72c1919981e0d3f11d9f3c4ab3df3a71dc4b0dd896a418736101`  
		Last Modified: Wed, 21 Jul 2021 00:31:23 GMT  
		Size: 3.7 MB (3654535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a57362c4e338c8a3a4e1a0403be2b787d94cd1b11bb42393675ed6da650b8bfb`  
		Last Modified: Wed, 21 Jul 2021 00:31:25 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
