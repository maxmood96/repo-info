## `golang:1-nanoserver-ltsc2022`

```console
$ docker pull golang@sha256:c71a6b3b94e044bf9d7bd17d0c9789db32584e679cd1aae5063645cb377ec458
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2340; amd64

### `golang:1-nanoserver-ltsc2022` - windows version 10.0.20348.2340; amd64

```console
$ docker pull golang@sha256:7ece3e0d63712d9f51c1a7f6fd977e0b87a21c2fced7c5ad302961c35ba83759
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.3 MB (192291313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1925ce42ce7b9da5de7113bf3053205014f97ae0101187a95632c1489fa69b26`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Tue, 05 Mar 2024 19:20:30 GMT
RUN Apply image 10.0.20348.2340
# Wed, 13 Mar 2024 01:56:18 GMT
SHELL [cmd /S /C]
# Wed, 13 Mar 2024 01:56:19 GMT
ENV GOPATH=C:\go
# Wed, 13 Mar 2024 01:56:20 GMT
USER ContainerAdministrator
# Wed, 13 Mar 2024 01:56:32 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Wed, 13 Mar 2024 01:56:32 GMT
USER ContainerUser
# Wed, 03 Apr 2024 17:05:25 GMT
ENV GOLANG_VERSION=1.22.2
# Wed, 03 Apr 2024 17:07:20 GMT
COPY dir:6a3197bc56362ded96b0930f47b7684fc93e6ac6a350b0206d0452f8fb599246 in C:\Program Files\Go 
# Wed, 03 Apr 2024 17:07:52 GMT
RUN go version
# Wed, 03 Apr 2024 17:07:52 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:94ec3b200bababb5c0b6605ad82c23779d8f918fbfe1ef5d1cf51be6f12fa749`  
		Last Modified: Tue, 12 Mar 2024 19:42:37 GMT  
		Size: 120.7 MB (120702694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0584fe58316f1cc0966e34105ef3c88ab19e6a95bdb41ca75cdf08cc88b290d5`  
		Last Modified: Wed, 13 Mar 2024 02:14:44 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55f3cffc7043949988f679565708042f3602ccd2565491acc56fd549f65849e6`  
		Last Modified: Wed, 13 Mar 2024 02:14:42 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13712b3bbb648bc53a820b1a3612e8ff4d45a163cabdf14b6e0bf1a7b147ee38`  
		Last Modified: Wed, 13 Mar 2024 02:14:42 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff2926f1f9e042fdbe7275aaa681c5e48d117dc8adfae105c96616f500bf9f0e`  
		Last Modified: Wed, 13 Mar 2024 02:14:42 GMT  
		Size: 88.1 KB (88092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5883de4f89867f6624e06cb05c3a3741e60dffdcd7674e46116e4057757e4b7b`  
		Last Modified: Wed, 13 Mar 2024 02:14:40 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85d7b6dd48acb65fabb3bda8514f11ad55e010b7aa848c15f7e52f06afb0ffb8`  
		Last Modified: Wed, 03 Apr 2024 17:25:03 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5b80bd747d0ae3bf3bd845c118c2498ddc44c62315890a4f1214deb829c39dd`  
		Last Modified: Wed, 03 Apr 2024 17:25:25 GMT  
		Size: 71.4 MB (71444354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e05314050185cbb79c275bddbd67e7dc336dd569f3580866d13bec844be9c425`  
		Last Modified: Wed, 03 Apr 2024 17:25:03 GMT  
		Size: 49.0 KB (48979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeb776f03bf542b2bf3b9df79ce2efaea96a3d9f90f14e011506cea20466b17c`  
		Last Modified: Wed, 03 Apr 2024 17:25:02 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
