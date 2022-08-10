## `eclipse-temurin:18-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:b097536997ffc8edb3afe338bf2056b4eb5fc60e1ed742ddbc8ee16730b35b5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.887; amd64

### `eclipse-temurin:18-nanoserver-ltsc2022` - windows version 10.0.20348.887; amd64

```console
$ docker pull eclipse-temurin@sha256:d78009058be1aeb24c83464b9c0e572e19062cd7f093c730288ec503ad5d2343
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.8 MB (304814445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52c9957c051690d4565bb8bb81b9d9723aca4082a88b21809d3a109de6db8f67`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 06 Aug 2022 18:05:23 GMT
RUN Apply image 10.0.20348.887
# Wed, 10 Aug 2022 16:28:17 GMT
SHELL [cmd /s /c]
# Wed, 10 Aug 2022 16:33:50 GMT
ENV JAVA_VERSION=jdk-18.0.2+9
# Wed, 10 Aug 2022 16:33:51 GMT
ENV JAVA_HOME=C:\openjdk-18
# Wed, 10 Aug 2022 16:33:52 GMT
USER ContainerAdministrator
# Wed, 10 Aug 2022 16:34:03 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 10 Aug 2022 16:34:04 GMT
USER ContainerUser
# Wed, 10 Aug 2022 16:34:19 GMT
COPY dir:fe0d9ce398e3d169055678c6642e68d763dc7a30e25c08274ab6c7ec599f7aba in C:\openjdk-18 
# Wed, 10 Aug 2022 16:34:33 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 10 Aug 2022 16:34:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2ebf439f800cd4c1fccaf4a0545e6bff60caa5141295c8ab81f6c525073c423d`  
		Size: 118.1 MB (118088450 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5f1e06146ab0490d235fe89786637467a4b71853ee428e8740ea6efbc536c47c`  
		Last Modified: Wed, 10 Aug 2022 16:48:40 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f13999e9467c86cf2ef854733e78081046c1b26eaee3ab579f32308a22ad3f2`  
		Last Modified: Wed, 10 Aug 2022 16:50:57 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:984aadb5c294a031eb9bf139e089a14953bfd160b9e3fb63c5407283f238f4b0`  
		Last Modified: Wed, 10 Aug 2022 16:50:57 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b8e890683ee09a276afb5655197ed4536d7af93add242ec3ef49a79370b553`  
		Last Modified: Wed, 10 Aug 2022 16:50:57 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b0017fc6b7e0fc882e7f2169bdf28cd916bdd5becfc60b3660f256cd4bdeb7f`  
		Last Modified: Wed, 10 Aug 2022 16:50:55 GMT  
		Size: 84.8 KB (84820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f5484fbab0fb42fe9cd48851c5207ac52537278b619798735df6ce414ff445b`  
		Last Modified: Wed, 10 Aug 2022 16:50:54 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42a183a1fe7904ad9094916997034bb713236ea12492576d6391c4d969fedff4`  
		Last Modified: Wed, 10 Aug 2022 16:51:13 GMT  
		Size: 186.6 MB (186571395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f481a0e3b0201a728db3d7ec94d4aa08f5a62bd78682a9264e21ebae6e2a38f`  
		Last Modified: Wed, 10 Aug 2022 16:50:54 GMT  
		Size: 62.8 KB (62795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f40c8235aaff932ddb56d70d6f332c2d4e8ef552bd75f2ea282bd021cf968a`  
		Last Modified: Wed, 10 Aug 2022 16:50:54 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
