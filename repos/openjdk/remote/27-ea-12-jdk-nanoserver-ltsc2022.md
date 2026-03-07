## `openjdk:27-ea-12-jdk-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:3eaa8d180f4eb4f6155129e04dbc4f0e0709d7aff8715c242e9408343a558310
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `openjdk:27-ea-12-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull openjdk@sha256:dda5ea7d2de04cb06fa65e206061255357973f3bf9deeb1cca0de0685c3a6524
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.2 MB (351200261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dba35452663c1c2795c7fffbce9d72d511f6f538e822926f87882842d706f5d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 06 Feb 2026 09:42:51 GMT
RUN Apply image 10.0.20348.4773
# Sat, 07 Mar 2026 01:08:34 GMT
SHELL [cmd /s /c]
# Sat, 07 Mar 2026 01:08:35 GMT
ENV JAVA_HOME=C:\openjdk-27
# Sat, 07 Mar 2026 01:08:35 GMT
USER ContainerAdministrator
# Sat, 07 Mar 2026 01:08:44 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Sat, 07 Mar 2026 01:08:45 GMT
USER ContainerUser
# Sat, 07 Mar 2026 01:08:45 GMT
ENV JAVA_VERSION=27-ea+12
# Sat, 07 Mar 2026 01:09:12 GMT
COPY dir:39bc387d6f4a82116c9105a5f2b625fb020bc268f5298b0afe5a9520fad3060e in C:\openjdk-27 
# Sat, 07 Mar 2026 01:09:22 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Sat, 07 Mar 2026 01:09:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ca0a97fd01c767a53a3e0856fa1db64de3eecf8d8b3f54cc7e6b032890bd7e7e`  
		Last Modified: Tue, 10 Feb 2026 19:28:47 GMT  
		Size: 126.6 MB (126645827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:733914e9336f66fcd203c4650be7967c8818f9bdfe1b2813812be0c698ef62b8`  
		Last Modified: Sat, 07 Mar 2026 01:09:28 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fda23e15514879db81c4848ed2e55780641852f49572f8b9e9fe191b826d77a`  
		Last Modified: Sat, 07 Mar 2026 01:09:28 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba2fd2f3be789594e0990b807acfc83bc75b35848ab3320005501a7372b8c3ed`  
		Last Modified: Sat, 07 Mar 2026 01:09:28 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10ca1c1c620b71a1d62f79529311bfeffe5532d5f994cf4900808267dec9817a`  
		Last Modified: Sat, 07 Mar 2026 01:09:28 GMT  
		Size: 83.0 KB (82951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:482449a376532a3e4c8ae030a387e1eb37b1265729f310c42ac0c3097ec221e3`  
		Last Modified: Sat, 07 Mar 2026 01:09:26 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f3ccd5c814c0ed6ac2eef3d80d33e15cc6aaadc1ee9b5825a4e3b54f2e58e74`  
		Last Modified: Sat, 07 Mar 2026 01:09:26 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:969e28703727d08fd5c5072231e843136f29457579fb51dced1b55cc0a907c92`  
		Last Modified: Sat, 07 Mar 2026 01:09:43 GMT  
		Size: 224.3 MB (224333957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e103f00e62bcda7b55a9d761515afab9ce26b924ab645614024e5e885d39ae7`  
		Last Modified: Sat, 07 Mar 2026 01:09:26 GMT  
		Size: 131.1 KB (131094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad2f83f8fdc62dbb097b0d84e993f529b3ee8454e426e25815783096e48af06c`  
		Last Modified: Sat, 07 Mar 2026 01:09:26 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
