## `golang:nanoserver`

```console
$ docker pull golang@sha256:4cf0043ca72ebd3c41cf55cfb0be5ded0f3b52dcc387266fd92aa38daf645f32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2402; amd64
	-	windows version 10.0.17763.5696; amd64

### `golang:nanoserver` - windows version 10.0.20348.2402; amd64

```console
$ docker pull golang@sha256:11f16e8e64150f9f2d8aab32111c7d34e4982fd8873b8f22c50659b78baebcb4
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.6 MB (192574113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:915f90580d558667de7e234257207986f10678bd427be2f8486be9b1cef3fdce`
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
# Wed, 10 Apr 2024 01:17:37 GMT
ENV GOLANG_VERSION=1.22.2
# Wed, 10 Apr 2024 01:19:34 GMT
COPY dir:6a3197bc56362ded96b0930f47b7684fc93e6ac6a350b0206d0452f8fb599246 in C:\Program Files\Go 
# Wed, 10 Apr 2024 01:19:54 GMT
RUN go version
# Wed, 10 Apr 2024 01:19:55 GMT
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
	-	`sha256:5b13f74cb8a5ad54c7da458b80d28e14fc6328f92d452c0d533c54b1a1090481`  
		Last Modified: Wed, 10 Apr 2024 01:35:55 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf9d9052750c3e662c6a846bcab7afef276591610a06378a4cf323fae857970b`  
		Last Modified: Wed, 10 Apr 2024 01:36:15 GMT  
		Size: 71.4 MB (71445473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e0ac32323d9123cc380eeadae150155b0c2634a6691ceb088dc0e381982572d`  
		Last Modified: Wed, 10 Apr 2024 01:35:55 GMT  
		Size: 50.4 KB (50447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78e418e83bec9df1a807864f1fec5f938461efd3550eac3f0cfba7654b5c88d0`  
		Last Modified: Wed, 10 Apr 2024 01:35:55 GMT  
		Size: 1.2 KB (1237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:nanoserver` - windows version 10.0.17763.5696; amd64

```console
$ docker pull golang@sha256:f1706960d8007e6e03cbf0c59e5cc9d1868c08fb7c5a0e6d765da929b2997fac
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.4 MB (176432895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa758437167d60e18ef5bd1d083b3f2649f5573bdccadfe408cc83adc0f1dccf`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sat, 06 Apr 2024 02:05:27 GMT
RUN Apply image 10.0.17763.5696
# Wed, 10 Apr 2024 01:20:05 GMT
SHELL [cmd /S /C]
# Wed, 10 Apr 2024 01:20:06 GMT
ENV GOPATH=C:\go
# Wed, 10 Apr 2024 01:20:06 GMT
USER ContainerAdministrator
# Wed, 10 Apr 2024 01:20:17 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Wed, 10 Apr 2024 01:20:18 GMT
USER ContainerUser
# Wed, 10 Apr 2024 01:20:19 GMT
ENV GOLANG_VERSION=1.22.2
# Wed, 10 Apr 2024 01:22:13 GMT
COPY dir:6a3197bc56362ded96b0930f47b7684fc93e6ac6a350b0206d0452f8fb599246 in C:\Program Files\Go 
# Wed, 10 Apr 2024 01:22:34 GMT
RUN go version
# Wed, 10 Apr 2024 01:22:35 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:a9b4234352dbe48c2ab26f66b300829ca94d2fc63738ee6d4221f9962d33cf5c`  
		Last Modified: Tue, 09 Apr 2024 20:38:39 GMT  
		Size: 104.9 MB (104889083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcbc22137e8bec78cc562f6e5ea99543a7a0a8e9da2a641f333f2363fe1dcd89`  
		Last Modified: Wed, 10 Apr 2024 01:36:29 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:456844b7ca82c547f7ab11f3e90de37eb3c5d97fa67719f9e410e440713de59a`  
		Last Modified: Wed, 10 Apr 2024 01:36:29 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:689ea0dff33b4cdbbab3b9fd19d416b1f38d22aa9f3755e7a976b414b5c045ad`  
		Last Modified: Wed, 10 Apr 2024 01:36:29 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4835ced22260031d04592970b9337ed60542e56b6c2aa31a239d2d4f1bbe4219`  
		Last Modified: Wed, 10 Apr 2024 01:36:29 GMT  
		Size: 66.2 KB (66221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77d5e2f5ce7618906cb0c792ce8d9fe2c1736b69b8b0e61810a7d7a83cd60510`  
		Last Modified: Wed, 10 Apr 2024 01:36:28 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa99397efd2c6d8ca598ec530f19fa07979e26ea7e6bdbb7b23817778f3f6a6a`  
		Last Modified: Wed, 10 Apr 2024 01:36:27 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eea5d1060cb43df95c55beea21e94497f428da5f9f808a52e4db527868dc0731`  
		Last Modified: Wed, 10 Apr 2024 01:36:47 GMT  
		Size: 71.4 MB (71398692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8161a552042f72d347adb8fe0e0b3828df1c6eba91c6d58c3fadbbe4c446f48`  
		Last Modified: Wed, 10 Apr 2024 01:36:27 GMT  
		Size: 72.3 KB (72252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f18583bfa4de362e8eed0ebab79d01c99aa8651624a6c85b9c2645e5176147c8`  
		Last Modified: Wed, 10 Apr 2024 01:36:27 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
