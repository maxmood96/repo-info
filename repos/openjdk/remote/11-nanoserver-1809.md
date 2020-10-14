## `openjdk:11-nanoserver-1809`

```console
$ docker pull openjdk@sha256:ad1798b5394903380e2b278a2efca1389e678b4fda263ad5ff02d570ba4d50fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1518; amd64

### `openjdk:11-nanoserver-1809` - windows version 10.0.17763.1518; amd64

```console
$ docker pull openjdk@sha256:81289f2e1ff5083354621d384a58150bf20c7b31ae108f4a5a066a1600336f9f
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.4 MB (291370176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37a881baba755a3d19cc136e9f47565be3348afb57b909d8360d87f62a56407e`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 30 Sep 2020 11:25:56 GMT
RUN Apply image 1809-amd64
# Wed, 14 Oct 2020 17:46:04 GMT
SHELL [cmd /s /c]
# Wed, 14 Oct 2020 18:09:37 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 14 Oct 2020 18:09:38 GMT
USER ContainerAdministrator
# Wed, 14 Oct 2020 18:09:49 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH%
# Wed, 14 Oct 2020 18:09:50 GMT
USER ContainerUser
# Wed, 14 Oct 2020 18:09:50 GMT
ENV JAVA_VERSION=11.0.8
# Wed, 14 Oct 2020 18:10:32 GMT
COPY dir:ba8f3626996a51913ed5e7f3fbcaeadaf7aaae17e19e9afdd11f176c2572b854 in C:\openjdk-11 
# Wed, 14 Oct 2020 18:10:49 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version
# Wed, 14 Oct 2020 18:10:50 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:aab6118ce69c93410df7fa15842a6e3b3c7ff20b639c779b5d5f78e7653eaa07`  
		Size: 101.2 MB (101205155 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:40f59dc77cd194db29e444ce30cc9a91a3d555f7d4d7329fb6f46c13e559dc2f`  
		Last Modified: Wed, 14 Oct 2020 18:31:55 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f71452a0f18412de182efba9576a5b92a0efc2e16153debf8e739bf4c49d106`  
		Last Modified: Wed, 14 Oct 2020 18:45:15 GMT  
		Size: 863.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e370e740589fe95eef0a7b3b8241434c87a065d1ce1e1a51c79380652a77c7a`  
		Last Modified: Wed, 14 Oct 2020 18:45:14 GMT  
		Size: 859.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71eb5aa4cac867a845c34f0b19641129ddabb68f8c9d58ca9e29fd4affd15493`  
		Last Modified: Wed, 14 Oct 2020 18:45:14 GMT  
		Size: 66.4 KB (66423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8b6875f38e605343500db154a6b0c205bbe14b43a316e36588ef7be179601e`  
		Last Modified: Wed, 14 Oct 2020 18:45:13 GMT  
		Size: 870.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:134c955122dc065f33b368957ce92d272083caaf6dd4f0945e56b8ad47bddd4f`  
		Last Modified: Wed, 14 Oct 2020 18:45:11 GMT  
		Size: 910.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0b289034b61327753465137f4db686aff04cc53b8c788ca9683d349ac25ffef`  
		Last Modified: Wed, 14 Oct 2020 18:48:43 GMT  
		Size: 190.0 MB (190038150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ead1e6fb5a2738989640d544ea17d422316accc98091afe96656aa0f11bfb7d4`  
		Last Modified: Wed, 14 Oct 2020 18:45:11 GMT  
		Size: 55.2 KB (55179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85d84f30d3da9419b1e0de91766ab084ac6ac219035eb85d9c5b39283761032e`  
		Last Modified: Wed, 14 Oct 2020 18:45:11 GMT  
		Size: 873.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
