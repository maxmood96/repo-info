## `golang:1-nanoserver-1809`

```console
$ docker pull golang@sha256:c62325a5a9c2ce1fd07abcc15ad0fcd43102408096bcb4b724415eb2a77c17ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `golang:1-nanoserver-1809` - windows version 10.0.17763.5458; amd64

```console
$ docker pull golang@sha256:1a7231373765928ff283814d3100eeccfaf54c63c7b7c194c9a51d88a54602d8
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.2 MB (176208187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00096a1d85cac0b93a6c01f062862c206b3d8bf3c9fda9d276a590539b8928c6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sun, 04 Feb 2024 03:35:01 GMT
RUN Apply image 10.0.17763.5458
# Wed, 14 Feb 2024 20:41:15 GMT
SHELL [cmd /S /C]
# Wed, 14 Feb 2024 20:41:16 GMT
ENV GOPATH=C:\go
# Wed, 14 Feb 2024 20:41:16 GMT
USER ContainerAdministrator
# Wed, 14 Feb 2024 20:41:28 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Wed, 14 Feb 2024 20:41:29 GMT
USER ContainerUser
# Tue, 05 Mar 2024 19:24:45 GMT
ENV GOLANG_VERSION=1.22.1
# Tue, 05 Mar 2024 19:26:45 GMT
COPY dir:ff4ed0e5730af1cd3210a0325ec904ffc63fb0554a3b82d7c5005a8b1ff65baa in C:\Program Files\Go 
# Tue, 05 Mar 2024 19:27:13 GMT
RUN go version
# Tue, 05 Mar 2024 19:27:14 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:81be0bec766f944241448cd25317f59edcb12514e41b43288302e3e88d5462ad`  
		Last Modified: Tue, 13 Feb 2024 20:17:19 GMT  
		Size: 104.6 MB (104621606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d248fdc6ec2b1d559770e63dd96445cd0911b26f5aa34668bd0f97d8dcbf30dc`  
		Last Modified: Wed, 14 Feb 2024 20:59:40 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6586f461b549b8a21faa95d36d7d137b98e16be3d4378291ed02e515a45d16a`  
		Last Modified: Wed, 14 Feb 2024 20:59:41 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db4a5e46c8ca02db6d6ce18763316cbc25eab61375eee1c1d30cb916693e7651`  
		Last Modified: Wed, 14 Feb 2024 20:59:40 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2de7f9916de5860d517b863d5d66cad66e2c53492daba2f203e310de3d375e81`  
		Last Modified: Wed, 14 Feb 2024 20:59:40 GMT  
		Size: 68.8 KB (68790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af6bbbec11a627dc9592bd963e17221216fb42732b6373e6b9722796eb69b04a`  
		Last Modified: Wed, 14 Feb 2024 20:59:38 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfc8cbac58d9bf9d5cc4e9018e88634ae9304210eeb297e34c7c62745f1647b5`  
		Last Modified: Tue, 05 Mar 2024 19:41:18 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bfb551f8dd1959ce13eef08a79975ecb23912c87685b213db280772bc395e8b`  
		Last Modified: Tue, 05 Mar 2024 19:41:38 GMT  
		Size: 71.4 MB (71438073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:278f520be330d14408087a92992f3d43dd4e7989df99a0134dec70ee831bb2e6`  
		Last Modified: Tue, 05 Mar 2024 19:41:18 GMT  
		Size: 72.5 KB (72482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7bff1ce620befe191953c82aa25d8543272bfe1785bd45b13fff797e61abdd1`  
		Last Modified: Tue, 05 Mar 2024 19:41:18 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
