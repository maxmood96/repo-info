## `golang:1-nanoserver-ltsc2022`

```console
$ docker pull golang@sha256:1bde7e03abc9cecfdceb3038b2c3c0eb6b638c65bbfcf95d54254bb2404590a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `golang:1-nanoserver-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull golang@sha256:0115cb4432072b92921b3bfc50cf1676e1ee7a080516751ab5d322904d65abdc
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.8 MB (184796218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52ad92dfaa64b7dff06f488fad95d859dd52ec7c99ef7ce68b2e34372ae6515e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 05 Sep 2025 12:57:47 GMT
RUN Apply image 10.0.20348.4171
# Mon, 13 Oct 2025 23:08:04 GMT
SHELL [cmd /S /C]
# Mon, 13 Oct 2025 23:08:04 GMT
ENV GOPATH=C:\go
# Mon, 13 Oct 2025 23:08:05 GMT
USER ContainerAdministrator
# Mon, 13 Oct 2025 23:08:14 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Mon, 13 Oct 2025 23:08:15 GMT
USER ContainerUser
# Mon, 13 Oct 2025 23:08:15 GMT
ENV GOLANG_VERSION=1.25.3
# Mon, 13 Oct 2025 23:09:47 GMT
COPY dir:6b7560915a38431967d90704d11f1201c2d1cdc45bff8fe429921d03a21c4716 in C:\Program Files\Go 
# Mon, 13 Oct 2025 23:09:50 GMT
RUN go version
# Mon, 13 Oct 2025 23:09:51 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:4d91bcff7058a4e51844e56c699b1d7293eed6bf0647068b736e15bccbb8e8ed`  
		Last Modified: Tue, 09 Sep 2025 17:40:59 GMT  
		Size: 122.7 MB (122719927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d1cdfd1411b540f20638465c293908c88709496fd262d8dea54382d2d31f13a`  
		Last Modified: Mon, 13 Oct 2025 23:10:13 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10f5bebce83ec448723325e3c343b2b57cd56b6e11cb0811cb9a8b24bb36965a`  
		Last Modified: Mon, 13 Oct 2025 23:10:13 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3737a185c47451884b5c24cd1511c5b0743ca322ee30c9cd6e6bde30b160140`  
		Last Modified: Mon, 13 Oct 2025 23:10:13 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98879990cc83d6284ea60d63c5f958c0b62495b9e06848be8bcf04d9019ecf99`  
		Last Modified: Mon, 13 Oct 2025 23:10:13 GMT  
		Size: 98.8 KB (98840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57b243ac6c429fe0eb4bfe16c0ae18c49d36ac235e071b92a828ed30b766f318`  
		Last Modified: Mon, 13 Oct 2025 23:10:13 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7eb0af1dd09ab963c05cdaacb45a336bba507344ba27d988b61cd8af09ecc07`  
		Last Modified: Mon, 13 Oct 2025 23:10:14 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c44b0881df2b3f3744fc3d9a57ebac851a5ea4ddfa2f0b6621b314376730666`  
		Last Modified: Mon, 13 Oct 2025 23:10:18 GMT  
		Size: 61.9 MB (61890295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19ac2bfdcf6c0434f2b4a0cb4169987d15c279268a3b9bda5abcd1fdd6a9db3a`  
		Last Modified: Mon, 13 Oct 2025 23:10:13 GMT  
		Size: 80.6 KB (80592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36552a47593ccd7901504d9937ae6fc6057f07dafa6f4f3e373370597e30ffae`  
		Last Modified: Mon, 13 Oct 2025 23:10:13 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
