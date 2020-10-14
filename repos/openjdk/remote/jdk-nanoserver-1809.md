## `openjdk:jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:0b8eb752118834ad0f526f58206b4b4d68617a41bca77af93ee2386a6d7a6629
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1518; amd64

### `openjdk:jdk-nanoserver-1809` - windows version 10.0.17763.1518; amd64

```console
$ docker pull openjdk@sha256:ae9519326439f71c201f59fd67d3ee54f17039aaa3a1ec72d7d7ed86268d2f59
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.1 MB (296148635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce2d130712e3bf241856ff814faf7f23ce3913e3e6d68ba47ce03a3361936606`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 30 Sep 2020 11:25:56 GMT
RUN Apply image 1809-amd64
# Wed, 14 Oct 2020 17:46:04 GMT
SHELL [cmd /s /c]
# Wed, 14 Oct 2020 17:53:54 GMT
ENV JAVA_HOME=C:\openjdk-15
# Wed, 14 Oct 2020 17:53:55 GMT
USER ContainerAdministrator
# Wed, 14 Oct 2020 17:54:05 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH%
# Wed, 14 Oct 2020 17:54:06 GMT
USER ContainerUser
# Wed, 14 Oct 2020 17:54:07 GMT
ENV JAVA_VERSION=15
# Wed, 14 Oct 2020 17:54:52 GMT
COPY dir:c7e08674451932ee3e39dd647bf57a58f604f71d6631e01f3c30405731e02d63 in C:\openjdk-15 
# Wed, 14 Oct 2020 17:55:11 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version
# Wed, 14 Oct 2020 17:55:12 GMT
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
	-	`sha256:9b8fff3aed0d31005e918a3cda7098b7efcfb1500d6289dd680cb51f9a47c246`  
		Last Modified: Wed, 14 Oct 2020 18:36:48 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d36a418005957c29e0c335992af9fba0f17c1d4089c5adbaa978023500d8cd24`  
		Last Modified: Wed, 14 Oct 2020 18:36:47 GMT  
		Size: 865.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80ea43fc075036898de3d3463d3a08fc3233dc8c60cd88bdaeba731f87bc100a`  
		Last Modified: Wed, 14 Oct 2020 18:36:47 GMT  
		Size: 63.5 KB (63525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a72f5407de4fd64ef89b53fc274578cafa71fb933276a39ee2c9dcb1a8c9b3`  
		Last Modified: Wed, 14 Oct 2020 18:36:44 GMT  
		Size: 860.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30bd48cb8170cc191a1037dcc7c2f6c9e86c8aa10a076803ddbda80c4273bf85`  
		Last Modified: Wed, 14 Oct 2020 18:36:44 GMT  
		Size: 864.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4ab859e4cbaa3f4f4615c42ace04a52d283f6560b9775ca7494c9de1e78a9f9`  
		Last Modified: Wed, 14 Oct 2020 18:37:20 GMT  
		Size: 191.4 MB (191359994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7244333c6b7e156e36fddcfa2ea37ff39b0a15ecdef76ee4491e4620e7858e3`  
		Last Modified: Wed, 14 Oct 2020 18:36:45 GMT  
		Size: 3.5 MB (3514673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14efffddef0e0c8dda4f03b09e896f8596e40cd19d6107c80967f5924ce9cc8f`  
		Last Modified: Wed, 14 Oct 2020 18:36:45 GMT  
		Size: 912.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
