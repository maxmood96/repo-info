## `golang:nanoserver`

```console
$ docker pull golang@sha256:013d987564f2e76e43118af9f44d2e3cf983a73ed588d88eebee7764d323361b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4349; amd64
	-	windows version 10.0.20348.3807; amd64

### `golang:nanoserver` - windows version 10.0.26100.4349; amd64

```console
$ docker pull golang@sha256:0f674d2633ab77e04cae9b5030acd1e2818ff57d09035cab21d9b5912111501d
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.2 MB (274171781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a7e0b7780575ac216bf0add8408dddc36f5118201955ec9c278f4ce29a23af0`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sat, 07 Jun 2025 15:19:59 GMT
RUN Apply image 10.0.26100.4349
# Tue, 08 Jul 2025 19:14:20 GMT
SHELL [cmd /S /C]
# Tue, 08 Jul 2025 19:14:21 GMT
ENV GOPATH=C:\go
# Tue, 08 Jul 2025 19:14:22 GMT
USER ContainerAdministrator
# Tue, 08 Jul 2025 19:14:25 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Tue, 08 Jul 2025 19:14:26 GMT
USER ContainerUser
# Tue, 08 Jul 2025 19:14:26 GMT
ENV GOLANG_VERSION=1.24.5
# Tue, 08 Jul 2025 19:15:44 GMT
COPY dir:a64a2923c1fcf6909ec85d25bc3e35bfa4572d72cc3eb98bcec274153f9f9413 in C:\Program Files\Go 
# Tue, 08 Jul 2025 19:15:47 GMT
RUN go version
# Tue, 08 Jul 2025 19:15:48 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:709fa8bff22087ae5c45c65a3b0777eb6ee12afd1b773aece2a322e84b66b1d1`  
		Last Modified: Tue, 10 Jun 2025 22:41:49 GMT  
		Size: 192.1 MB (192082516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:158d843bc3ed17eaebb1957dae9e591564b97db81550c30c1fc65863b649ffc6`  
		Last Modified: Tue, 08 Jul 2025 20:24:28 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:692f033468ed1d6f6e889ca38682faf9d61c02bddf36c1eb448aa9e102382fce`  
		Last Modified: Tue, 08 Jul 2025 20:24:28 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e18148295b9f708b61f263ad1d586830032dfc57678aec5da8c168e1b0c63fb`  
		Last Modified: Tue, 08 Jul 2025 20:24:28 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9098d43cf54306c25f08bc5278f6015aeebdd5d18e0a54acc5ddac8e0a081c23`  
		Last Modified: Tue, 08 Jul 2025 20:24:28 GMT  
		Size: 76.0 KB (76048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28c2fcfeab7f0be3682deeec06950612a19ff35f50cd68fbdd93391619d438a0`  
		Last Modified: Tue, 08 Jul 2025 20:24:28 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed92f20c416cc178f343238682447dc0e5eb1e8fe5b000a749e27adc3cd14cd0`  
		Last Modified: Tue, 08 Jul 2025 20:24:29 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:912030ee7e37cccedbe7b97ba3e0bf2c50c4d11b1183e088eb2e42fc18962183`  
		Last Modified: Tue, 08 Jul 2025 20:24:35 GMT  
		Size: 81.9 MB (81918330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd1d6bd355d4bd61e113fbe71f47c8281ea4d837a565e3412fb3b5c0db7f30f0`  
		Last Modified: Tue, 08 Jul 2025 20:24:29 GMT  
		Size: 88.4 KB (88364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1afff2c4ab7233e4a352f35616353851891ac38f4908c51d29154d271841216e`  
		Last Modified: Tue, 08 Jul 2025 20:24:29 GMT  
		Size: 1.2 KB (1235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:nanoserver` - windows version 10.0.20348.3807; amd64

```console
$ docker pull golang@sha256:95c57d6b859731a8806d686a805753590981db14d7a8d9242224939487f3aaac
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.6 MB (204600362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea318758afee55518db65e11ca790a2bae08bc6ce14e8c6e1eaeb17df4e0bb13`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 05 Jun 2025 00:43:46 GMT
RUN Apply image 10.0.20348.3807
# Tue, 08 Jul 2025 19:09:21 GMT
SHELL [cmd /S /C]
# Tue, 08 Jul 2025 19:09:22 GMT
ENV GOPATH=C:\go
# Tue, 08 Jul 2025 19:09:23 GMT
USER ContainerAdministrator
# Tue, 08 Jul 2025 19:09:29 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Tue, 08 Jul 2025 19:09:30 GMT
USER ContainerUser
# Tue, 08 Jul 2025 19:09:31 GMT
ENV GOLANG_VERSION=1.24.5
# Tue, 08 Jul 2025 19:11:12 GMT
COPY dir:a64a2923c1fcf6909ec85d25bc3e35bfa4572d72cc3eb98bcec274153f9f9413 in C:\Program Files\Go 
# Tue, 08 Jul 2025 19:11:16 GMT
RUN go version
# Tue, 08 Jul 2025 19:11:18 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:96acbf1c6d5b6cc37517502ecbb6a1d2eb55b7615b696401ead868c97a971964`  
		Last Modified: Tue, 10 Jun 2025 20:17:56 GMT  
		Size: 122.5 MB (122540534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d56c6d1db6280f129a4358f5af608f4d995f4772144c6ef46f69d8630e0159`  
		Last Modified: Tue, 08 Jul 2025 20:24:26 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e9467c652b9f3add098ae83593a7211037246fe7021dcababe2ff0d5c3c331`  
		Last Modified: Tue, 08 Jul 2025 20:24:26 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee4e18937d39bb651bd0cf00f166d59fb60329b2fd750398f3d38a37cb88005d`  
		Last Modified: Tue, 08 Jul 2025 20:24:26 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef85ba1e1cdf1278116099496b297c919938d867703eb963203000bb9e3a3d3a`  
		Last Modified: Tue, 08 Jul 2025 20:24:29 GMT  
		Size: 78.9 KB (78948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:171a73513bbcad1ccec25d843fb0e978ab242cfc3ce8208d537c48a18a517c07`  
		Last Modified: Tue, 08 Jul 2025 20:24:26 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2bf827412d0a0bcac69c531df3b073997cf9a4e74c873c015d3c266ce702c5f`  
		Last Modified: Tue, 08 Jul 2025 20:24:27 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d09fd56d0ea4851bbc13c1644939f8907025a3cb7f2a42676020d69fb4ab0b`  
		Last Modified: Tue, 08 Jul 2025 20:24:31 GMT  
		Size: 81.9 MB (81892100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c912155da0bdc83025b3e008beac7f8397a20e5c7bec51ab492d3b8f47885cf4`  
		Last Modified: Tue, 08 Jul 2025 20:24:27 GMT  
		Size: 82.3 KB (82301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:078358bcfba9d2b97aad2aaee519f5958625c569f74d2f2a69342f160ea3c382`  
		Last Modified: Tue, 08 Jul 2025 20:24:27 GMT  
		Size: 1.2 KB (1233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
