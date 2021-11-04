## `golang:1-nanoserver`

```console
$ docker pull golang@sha256:6bc57ff627849b5231bf1b1c900a76634fe6dbddbd168335f2f74d58e9e452c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.288; amd64
	-	windows version 10.0.17763.2237; amd64

### `golang:1-nanoserver` - windows version 10.0.20348.288; amd64

```console
$ docker pull golang@sha256:a72dcc50a83894f30966b404178707a65117ecebbdbb38b28f943fe1264937eb
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.1 MB (262149019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bff953c86d2e0b586e6ded65b8ded9d31e2f951141e9a7c10338f81530327f38`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 07 Oct 2021 11:15:04 GMT
RUN Apply image ltsc2022-amd64
# Wed, 13 Oct 2021 12:48:50 GMT
SHELL [cmd /S /C]
# Wed, 13 Oct 2021 12:48:51 GMT
ENV GOPATH=C:\go
# Wed, 13 Oct 2021 12:48:52 GMT
USER ContainerAdministrator
# Wed, 13 Oct 2021 12:49:42 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Wed, 13 Oct 2021 12:49:43 GMT
USER ContainerUser
# Thu, 04 Nov 2021 20:25:35 GMT
ENV GOLANG_VERSION=1.17.3
# Thu, 04 Nov 2021 20:27:49 GMT
COPY dir:109abd4b7de9c681888d02224b53efb3555fcce4cf01c933658c41331cc240cb in C:\Program Files\Go 
# Thu, 04 Nov 2021 20:28:42 GMT
RUN go version
# Thu, 04 Nov 2021 20:28:42 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:91284e7e8fd4bd7ebcfa98544a3e4f59639f38281225c81c34b6fe22e0dba4e5`  
		Size: 116.9 MB (116939483 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:20e7750a023cb83652c7a9fb1fa59842126978ee34af47a4d3ed0508abf4b266`  
		Last Modified: Wed, 13 Oct 2021 13:28:53 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:823dac1744a93be130acef2018641dda84d663debf8462412c9904299eed4bdf`  
		Last Modified: Wed, 13 Oct 2021 13:28:53 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d3069ffd7a6649bf4acfceddd27a7177a71566770ca5e5aecbfe8daee26a6f1`  
		Last Modified: Wed, 13 Oct 2021 13:28:52 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0226fc2bbb1dd690934fb2d69ed72106e4b21592b4edb1d373d14d7e7c26ab1f`  
		Last Modified: Wed, 13 Oct 2021 13:28:52 GMT  
		Size: 78.5 KB (78477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90eae1289df0e0aa2e12d0696ad2612e614fc07bb39dbf50dc4a6ae357fed75c`  
		Last Modified: Wed, 13 Oct 2021 13:28:50 GMT  
		Size: 1.1 KB (1143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afe7b8ecb9645ab4eb87794bc7301da08b4d11b68bbee33856cf133bb8a90b3f`  
		Last Modified: Thu, 04 Nov 2021 20:51:19 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:200db483bc3e9a741606e92bd3621a184ee76358f86834c2561fc2bce9a20198`  
		Last Modified: Thu, 04 Nov 2021 20:53:58 GMT  
		Size: 145.1 MB (145076913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6a3744729b9faaf08c059ec5d42a68b6753407d07a0b1439aa4a2dd9f3ffe08`  
		Last Modified: Thu, 04 Nov 2021 20:51:19 GMT  
		Size: 47.1 KB (47103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48bd9fa47ddd1d7941b799bdba60cea04ecd62dfce0fd2bee7877d2e8414460c`  
		Last Modified: Thu, 04 Nov 2021 20:51:19 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-nanoserver` - windows version 10.0.17763.2237; amd64

```console
$ docker pull golang@sha256:473b364ae95d664bcaf43231a0dfb3d9936f8e65c442c323d13785134c3eb249
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.8 MB (247847340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8aca9e3dec3dafa837e6dc9195b6f5d607332b3260ed42f09a878c436e18310`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 07 Oct 2021 08:01:14 GMT
RUN Apply image 1809-amd64
# Wed, 13 Oct 2021 12:53:34 GMT
SHELL [cmd /S /C]
# Wed, 13 Oct 2021 12:53:35 GMT
ENV GOPATH=C:\go
# Wed, 13 Oct 2021 12:53:36 GMT
USER ContainerAdministrator
# Wed, 13 Oct 2021 12:54:21 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Wed, 13 Oct 2021 12:54:22 GMT
USER ContainerUser
# Thu, 04 Nov 2021 20:28:50 GMT
ENV GOLANG_VERSION=1.17.3
# Thu, 04 Nov 2021 20:31:05 GMT
COPY dir:109abd4b7de9c681888d02224b53efb3555fcce4cf01c933658c41331cc240cb in C:\Program Files\Go 
# Thu, 04 Nov 2021 20:31:49 GMT
RUN go version
# Thu, 04 Nov 2021 20:31:49 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:934e212983f208dc2bebc5de38259a6a62f1761868aacfee2cb3585a13b1e24b`  
		Size: 102.7 MB (102661372 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:372f5dac265602794d3a4ddc20bd9845caf2acda0cec410704843c213a880da9`  
		Last Modified: Wed, 13 Oct 2021 13:29:46 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:183500fddc25e2dfe8ccd0711855ed60cf6ed8ea79a9a35d229e1404dcee495b`  
		Last Modified: Wed, 13 Oct 2021 13:29:45 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd0fba843b7bfbab4c85a2bdddee6edca9a1abd62fd3a79f749ed662d3ce9cc`  
		Last Modified: Wed, 13 Oct 2021 13:29:46 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97c71d616b79e5a5e1dc3c1bb13ae2c58cf3038ecc454f7114a77189d1958c02`  
		Last Modified: Wed, 13 Oct 2021 13:29:45 GMT  
		Size: 71.4 KB (71390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d3f6872895200118f75543b31ccf5e8daa945cfaf05b3ab505bbe84f7f15a42`  
		Last Modified: Wed, 13 Oct 2021 13:29:43 GMT  
		Size: 1.1 KB (1117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d54ac2eac012e3796270bb112fb83e47766fa12903f61c0a59a134e8b0e5312`  
		Last Modified: Thu, 04 Nov 2021 20:54:14 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d67e6e5ad21fa3844df3850ef7ba55e281afad9bdf79d0fb26489edd594ec62f`  
		Last Modified: Thu, 04 Nov 2021 20:56:51 GMT  
		Size: 145.1 MB (145065441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0daf805c056a62019475cbc922de2eba57c05fc333e83199f31f122dbbb29c4`  
		Last Modified: Thu, 04 Nov 2021 20:54:14 GMT  
		Size: 42.0 KB (42050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf116623ee16f83036738ebfeba32cceebaa1a7fd9d365ec4948929de10bb2d9`  
		Last Modified: Thu, 04 Nov 2021 20:54:14 GMT  
		Size: 1.4 KB (1385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
