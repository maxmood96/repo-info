## `openjdk:14-ea-26-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:87a608e88849a3c11ef5a72950105991e49608f9451f64b14419a72518762bf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.914; amd64

### `openjdk:14-ea-26-jdk-nanoserver-1809` - windows version 10.0.17763.914; amd64

```console
$ docker pull openjdk@sha256:0a755fd3d7a7c4a987970aff2a7d5684a0864b6048bda1412c77992d0f465ced
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.8 MB (297849499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dfbb0db8b4ad6fe5023a54eddff8db973aa3477901cfa6eb0017713f23979d3`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 28 Nov 2019 13:16:41 GMT
RUN Apply image 1809-amd64
# Wed, 11 Dec 2019 18:49:48 GMT
SHELL [cmd /s /c]
# Wed, 11 Dec 2019 18:49:50 GMT
ENV JAVA_HOME=C:\openjdk-14
# Wed, 11 Dec 2019 18:49:51 GMT
USER ContainerAdministrator
# Wed, 11 Dec 2019 18:50:06 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH%
# Wed, 11 Dec 2019 18:50:07 GMT
USER ContainerUser
# Wed, 11 Dec 2019 18:50:08 GMT
ENV JAVA_VERSION=14-ea+26
# Wed, 11 Dec 2019 18:51:14 GMT
COPY dir:ae2c3890b7d3acb247eb18056cb2441c65050a4d8ec50a06fedcb1bc8a146371 in C:\openjdk-14 
# Wed, 11 Dec 2019 18:51:33 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version
# Wed, 11 Dec 2019 18:51:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1951f408509ba9ddcf240ef5d838c72c5596f97a05b063446508f2ba15d510f2`  
		Size: 101.1 MB (101106116 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:163d55b77f49371136083ba8066ddbec4afad6e1f4fbba77fa4ffebc99a8098a`  
		Last Modified: Wed, 11 Dec 2019 20:01:21 GMT  
		Size: 945.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9326e4caa8f459874d77c281820948a0fa2e558568f484250684f714e368c0bc`  
		Last Modified: Wed, 11 Dec 2019 20:01:19 GMT  
		Size: 953.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c07bbc07ec7d9f59279b56946327222e61b8d576bc34eb8b70be4aa88b484d87`  
		Last Modified: Wed, 11 Dec 2019 20:01:19 GMT  
		Size: 944.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c25567424a9bb0685aa9d0cc78a53b800a3447fff914466146890e6bf40dcdd`  
		Last Modified: Wed, 11 Dec 2019 20:01:19 GMT  
		Size: 63.9 KB (63920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6607ef629cd6ba3de9b2b3f57cdc6172ca483c4f285428321d4b04ce9b321db8`  
		Last Modified: Wed, 11 Dec 2019 20:01:16 GMT  
		Size: 949.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c741c9f2e6abd9f6dc49049da1cef30e5682173df806874f7511e9be2abbe4d`  
		Last Modified: Wed, 11 Dec 2019 20:01:16 GMT  
		Size: 920.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:847d214a32bac175216d1f8234d6aa84e1c438418a26d5ec6867f346592b2355`  
		Last Modified: Wed, 11 Dec 2019 20:01:38 GMT  
		Size: 193.2 MB (193233501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0927c172fa286b01b75dc510aa398dd3f11741dc96489ddb9cb8ef28add1c23`  
		Last Modified: Wed, 11 Dec 2019 20:01:18 GMT  
		Size: 3.4 MB (3440325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b92493ab53dfedbfee84b285bbf993f6eb689f079df2c91b53d0644210570ed`  
		Last Modified: Wed, 11 Dec 2019 20:01:16 GMT  
		Size: 926.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
