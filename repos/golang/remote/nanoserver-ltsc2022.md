## `golang:nanoserver-ltsc2022`

```console
$ docker pull golang@sha256:0b8935555f09ae9b1ac6d261979fec84f7aa089c38d9f5eec319ec1742173233
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2402; amd64

### `golang:nanoserver-ltsc2022` - windows version 10.0.20348.2402; amd64

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
