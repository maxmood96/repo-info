## `golang:nanoserver`

```console
$ docker pull golang@sha256:25340a50bc56190a6ee21f931480b3f35ff738fde7cd3c00c1d75da7cfdfdfb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2529; amd64
	-	windows version 10.0.17763.5936; amd64

### `golang:nanoserver` - windows version 10.0.20348.2529; amd64

```console
$ docker pull golang@sha256:0ffab067c36442166a922477dc04bc7378a5c6da0188af9d397b8e112d3946d1
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (192026499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:466e9f3158b8ee1f3768da7c187bcef39f0856289bf9a82c3dc26d79960a435d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Wed, 19 Jun 2024 19:27:30 GMT
RUN Apply image 10.0.20348.2529
# Sat, 22 Jun 2024 00:59:34 GMT
SHELL [cmd /S /C]
# Sat, 22 Jun 2024 00:59:35 GMT
ENV GOPATH=C:\go
# Sat, 22 Jun 2024 00:59:36 GMT
USER ContainerAdministrator
# Sat, 22 Jun 2024 00:59:38 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Sat, 22 Jun 2024 00:59:39 GMT
USER ContainerUser
# Sat, 22 Jun 2024 00:59:39 GMT
ENV GOLANG_VERSION=1.22.4
# Sat, 22 Jun 2024 01:00:44 GMT
COPY dir:5740e62168801895135af54bbf9a0c0e6996b1c9f19a0a4d6d32e83e842d4de4 in C:\Program Files\Go 
# Sat, 22 Jun 2024 01:00:47 GMT
RUN go version
# Sat, 22 Jun 2024 01:00:47 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:a8c295c425a912de308ded279124ae45fec44d55a451843fe5877155417f453c`  
		Last Modified: Fri, 21 Jun 2024 02:24:34 GMT  
		Size: 120.5 MB (120499549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ea6db58a69b0fc6164299ace8d0b6dd6b5a01db07f3b41bdc38e789028399cd`  
		Last Modified: Sat, 22 Jun 2024 01:00:54 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:151dbfab81989071d8242fe6ba2928446101745c82ca6d78d2605cc5dbdfb32b`  
		Last Modified: Sat, 22 Jun 2024 01:00:54 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:425156bae49448d75b58d7e4fafa31f443a556d9fa73c25613d89b10e7e995d3`  
		Last Modified: Sat, 22 Jun 2024 01:00:53 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3686fd5110779a2e2a9f831d091ec391b306a0c0f08450ca2ac042b6ab2c01`  
		Last Modified: Sat, 22 Jun 2024 01:00:53 GMT  
		Size: 76.2 KB (76160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b7b10641bc3e380aebdb73ad728895430277aaaf0ffea3fe552f0b00f0bd164`  
		Last Modified: Sat, 22 Jun 2024 01:00:52 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b8716bdf43a2eb4e1264a11dc8ad2fb5636407f821e52583cc38f636914e068`  
		Last Modified: Sat, 22 Jun 2024 01:00:52 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d0016f18174a9de9d6012bb12b3b860337b9215b1c50f95de19b3c8fcf21d85`  
		Last Modified: Sat, 22 Jun 2024 01:01:02 GMT  
		Size: 71.4 MB (71355570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:056c08b924ee5c0dcbf6dfb82390ea51fdaddea87e0c3da5cf0727c2f4d8278d`  
		Last Modified: Sat, 22 Jun 2024 01:00:52 GMT  
		Size: 88.8 KB (88799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bde6ec97b1be6b5df9692e15ecebb337425509e2933ebafc3932372c19a405e`  
		Last Modified: Sat, 22 Jun 2024 01:00:52 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:nanoserver` - windows version 10.0.17763.5936; amd64

```console
$ docker pull golang@sha256:7af7cfa9740e11079241e58eaa30911fbed9214352add0b883e7a38e9e2d6c58
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.5 MB (226537406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f5410d1787af7e74a8f87622d07f5cabd992b13ff4115b201398c213395606f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 07 Jun 2024 10:54:05 GMT
RUN Apply image 10.0.17763.5936
# Wed, 12 Jun 2024 19:12:50 GMT
SHELL [cmd /S /C]
# Wed, 12 Jun 2024 19:12:52 GMT
ENV GOPATH=C:\go
# Wed, 12 Jun 2024 19:12:53 GMT
USER ContainerAdministrator
# Wed, 12 Jun 2024 19:12:55 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Wed, 12 Jun 2024 19:12:55 GMT
USER ContainerUser
# Wed, 12 Jun 2024 19:12:56 GMT
ENV GOLANG_VERSION=1.22.4
# Wed, 12 Jun 2024 19:13:52 GMT
COPY dir:5740e62168801895135af54bbf9a0c0e6996b1c9f19a0a4d6d32e83e842d4de4 in C:\Program Files\Go 
# Wed, 12 Jun 2024 19:13:55 GMT
RUN go version
# Wed, 12 Jun 2024 19:13:56 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:4f703ea968d7f7434cf61e5d835cb3c507a6364ff8c7b3b96b73391b22115615`  
		Last Modified: Tue, 11 Jun 2024 20:35:02 GMT  
		Size: 155.0 MB (155033193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1d628bb1d91a858e5063e1d69cc7ba8113ed9edcc872b849bdc0a0475c4b268`  
		Last Modified: Wed, 12 Jun 2024 19:14:00 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60bb9c1672ba31ae0a7602d58f118ee7417c5dc2867cfc93026c8f0a7758bb56`  
		Last Modified: Wed, 12 Jun 2024 19:13:59 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:713588898df43a603042b9513c70aef40f2e83bef5bb21a23d1a757e5df05c03`  
		Last Modified: Wed, 12 Jun 2024 19:13:59 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9444e67aac4b3b446c3d2f276cb2a7bc66d21d4ed15aebc2bb25f1e19448c1a`  
		Last Modified: Wed, 12 Jun 2024 19:13:59 GMT  
		Size: 71.7 KB (71677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d193708da25c09631a52f0e1e359fe14ce08e812fead8e02e8f17a863b69d81c`  
		Last Modified: Wed, 12 Jun 2024 19:13:58 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73fe1348b2c40e55497cea2f15356a6a19e1613976bf126857809918de391c30`  
		Last Modified: Wed, 12 Jun 2024 19:13:58 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12cc983616b1478116d7e6e745e29786db953ebc0e713e3961eaebb92ae6187d`  
		Last Modified: Wed, 12 Jun 2024 19:14:09 GMT  
		Size: 71.4 MB (71356064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fdfed97dbc9989debcf2f9820020b447e713a8297960fac0234aafeacb8ba2e`  
		Last Modified: Wed, 12 Jun 2024 19:13:58 GMT  
		Size: 69.9 KB (69883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:925e580a5b6857a0ad5e76439ead13bde9aa458082ed25249bc1779058107ce3`  
		Last Modified: Wed, 12 Jun 2024 19:13:58 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
