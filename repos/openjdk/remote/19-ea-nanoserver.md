## `openjdk:19-ea-nanoserver`

```console
$ docker pull openjdk@sha256:ef02af16308b5f7045f1452206437ea1aae4daa6ff49cd72a80cb5563e874299
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2565; amd64

### `openjdk:19-ea-nanoserver` - windows version 10.0.17763.2565; amd64

```console
$ docker pull openjdk@sha256:3030664efae0ba04f9dad6dc93d7170eabb2f654c10447bf9706f21c48fb6d5a
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.5 MB (294472160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a984141c26b85fed543e95efbffd1c00b969e6650fa954bbc598d1b202dd7b29`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 02 Feb 2022 19:06:51 GMT
RUN Apply image 1809-amd64
# Wed, 09 Feb 2022 18:45:32 GMT
SHELL [cmd /s /c]
# Wed, 09 Feb 2022 18:45:33 GMT
ENV JAVA_HOME=C:\openjdk-19
# Wed, 09 Feb 2022 18:45:33 GMT
USER ContainerAdministrator
# Wed, 09 Feb 2022 18:45:46 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 09 Feb 2022 18:45:47 GMT
USER ContainerUser
# Wed, 02 Mar 2022 01:19:51 GMT
ENV JAVA_VERSION=19-ea+11
# Wed, 02 Mar 2022 01:20:05 GMT
COPY dir:f617d909fae19b9e0ec4e00742e0df9a9edfca9817314e0fe21998a6cb11f72d in C:\openjdk-19 
# Wed, 02 Mar 2022 01:20:29 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 02 Mar 2022 01:20:30 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bd0b37167cd3d731eb15196e123df7156b5a35597874d3016a1a4298c46fac3f`  
		Size: 103.1 MB (103087119 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5a7f567e84a5a148036156650a47ef7eec0187f17e880d3b475e51dacd70077b`  
		Last Modified: Wed, 09 Feb 2022 19:20:50 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e69acde47ea38ca917ac70bd099e8642e4d106e4d031254a5bd61c52e9e93a26`  
		Last Modified: Wed, 09 Feb 2022 19:20:50 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51a983d7a89070a62890b5312d217fb42c0a23a81f4b88020f86dd774b681bd5`  
		Last Modified: Wed, 09 Feb 2022 19:20:50 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:798ff236fae94b7a9651e0beb7fde720729c184b3d3150895ba4d507d0b4794b`  
		Last Modified: Wed, 09 Feb 2022 19:20:49 GMT  
		Size: 77.7 KB (77739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b819309b74b4730666b4d3b76627010d142d418aa74b8068c4e4af5d3d77b23`  
		Last Modified: Wed, 09 Feb 2022 19:20:47 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3066b6b53bd8d891ef908e6c5cdc77c3ba2e2cf390f1f1eaa253ce0d55e92cc3`  
		Last Modified: Wed, 02 Mar 2022 03:22:30 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37b4ff107be3d3d73cabab3e8404b05244e09f8195daf0406cfd65830006e515`  
		Last Modified: Wed, 02 Mar 2022 03:25:54 GMT  
		Size: 187.8 MB (187760475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e98459b84ce434273cea0184f52db716d6f3ac699247390f5e96195fb9564fa`  
		Last Modified: Wed, 02 Mar 2022 03:22:31 GMT  
		Size: 3.5 MB (3539912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a72fa080e99db2b106f79a90b0c57218dfe957bd710e425d2c3bf0bae60119e`  
		Last Modified: Wed, 02 Mar 2022 03:22:30 GMT  
		Size: 1.1 KB (1143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
