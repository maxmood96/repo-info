## `golang:1-nanoserver-ltsc2022`

```console
$ docker pull golang@sha256:1a7c49ea03c8ae682233d81c65bd690c7cbfa32ab4a0b1d0ff3a52aa515207d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2402; amd64

### `golang:1-nanoserver-ltsc2022` - windows version 10.0.20348.2402; amd64

```console
$ docker pull golang@sha256:a4d31ced8d21bd6db85378a3637cd89992b08a3b4f6bbd5fdb438eff55e362ad
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.5 MB (192518077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de941d9b425831581d6d7382e423fafe378e69a4626b10d11875bc9f30a68bd7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 05 Apr 2024 08:53:11 GMT
RUN Apply image 10.0.20348.2402
# Wed, 10 Apr 2024 01:17:21 GMT
SHELL [cmd /S /C]
# Wed, 10 Apr 2024 01:17:21 GMT
ENV GOPATH=C:\go
# Wed, 10 Apr 2024 01:17:22 GMT
USER ContainerAdministrator
# Wed, 10 Apr 2024 01:17:36 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Wed, 10 Apr 2024 01:17:37 GMT
USER ContainerUser
# Tue, 07 May 2024 18:22:14 GMT
ENV GOLANG_VERSION=1.22.3
# Tue, 07 May 2024 18:24:10 GMT
COPY dir:ffa8536da1cb924e452c58fab6629a557d0fc4fd3762105d4438f5276ea51d56 in C:\Program Files\Go 
# Tue, 07 May 2024 18:24:30 GMT
RUN go version
# Tue, 07 May 2024 18:24:31 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:755fc767289b8847bd0d0d8d75efc308c040140acf2a3426973ba9fbf022c4c0`  
		Last Modified: Tue, 09 Apr 2024 23:50:18 GMT  
		Size: 121.0 MB (120993754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66dcbea5316fcd69728488160af3506f2a33dc1c8429fb8f73eaa617b13123d4`  
		Last Modified: Wed, 10 Apr 2024 01:35:58 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef36a16de903bbad6a57efac63fe5a882093e068ee08fa6c85fd3ba2259109b4`  
		Last Modified: Wed, 10 Apr 2024 01:35:57 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d9e4e46f0c5a2ef2556051cae44ffdd6ac787ff01286e8b51733f43f11fc197`  
		Last Modified: Wed, 10 Apr 2024 01:35:57 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d200757a0cb0820ee28356854e2155015295216e3372beee6c3bf38bb2e85dc4`  
		Last Modified: Wed, 10 Apr 2024 01:35:57 GMT  
		Size: 77.4 KB (77363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32fe699bb42c33fce2c45eabed1a4cc2db93955d652228008b8ba010bafddf83`  
		Last Modified: Wed, 10 Apr 2024 01:35:55 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1246b8e73b13622530720aff7ced5176da4db276497bded2750319ee6bdc3a`  
		Last Modified: Tue, 07 May 2024 18:40:39 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8468027a1e5ca9aefd7c0f29417e3d42c871502014ad95230e3daa93c473860d`  
		Last Modified: Tue, 07 May 2024 18:40:59 GMT  
		Size: 71.4 MB (71388917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fff3dec398a9617a38768ca3009ae0f0895697deb7975d82f77fced7068718f5`  
		Last Modified: Tue, 07 May 2024 18:40:39 GMT  
		Size: 51.1 KB (51063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e7785344300719e8343b67ceade8807728914329abe6fd6107253702d4146b1`  
		Last Modified: Tue, 07 May 2024 18:40:39 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
