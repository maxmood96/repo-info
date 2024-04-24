## `telegraf:latest`

```console
$ docker pull telegraf@sha256:75af50d15b462c1ad679efd831c98a7d1322cf7f94f34e0b7267f9b45973f4df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:latest` - linux; amd64

```console
$ docker pull telegraf@sha256:7b4d3285c9263ddf956c181c072f7152aedd385b7b376600878e4f577bab19f8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.8 MB (154783671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a70d2f3a9dda678871a1d15135c50ad731e32de112d3a58a1635a537fc97c259`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 Apr 2024 01:50:34 GMT
ADD file:ca6d1f0f80dd6c91b8ba1d1adf77d7af6d0e5f2f493a2858e384c11874314395 in / 
# Wed, 10 Apr 2024 01:50:35 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 05:24:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 17:16:34 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 17:16:35 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Mon, 22 Apr 2024 22:25:42 GMT
ENV TELEGRAF_VERSION=1.30.2
# Mon, 22 Apr 2024 22:25:47 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Mon, 22 Apr 2024 22:25:47 GMT
EXPOSE 8092/udp 8094 8125/udp
# Mon, 22 Apr 2024 22:25:47 GMT
COPY file:3d723e9d10409fb06c7eaa4bbebe18017fc82dee6330d688adb684b64917f206 in /entrypoint.sh 
# Mon, 22 Apr 2024 22:25:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Apr 2024 22:25:47 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:609c73876867487da051ad470002217da69bb052e2538710ade0730d893ff51f`  
		Last Modified: Wed, 10 Apr 2024 01:55:11 GMT  
		Size: 49.6 MB (49560360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7247ea8d81e671d079d67f3a9909315ef4641b45db90d62a1b18e3430c1937d4`  
		Last Modified: Wed, 10 Apr 2024 05:34:49 GMT  
		Size: 24.0 MB (24046793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c65925cef157ec92ca4ac7ea2fee498997e6f04ceabcc6f5ba6ceec5ff79712`  
		Last Modified: Wed, 10 Apr 2024 17:17:26 GMT  
		Size: 19.2 MB (19151211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e46883b5de031b19b1f858d24ef5c262d06bb7b3105c84db483d710445599e8`  
		Last Modified: Wed, 10 Apr 2024 17:17:23 GMT  
		Size: 1.8 KB (1814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b08f004667eb3b18c3e49371bc700008325d69e2a9cc5b513852fd8f65439b5`  
		Last Modified: Mon, 22 Apr 2024 22:26:28 GMT  
		Size: 62.0 MB (62022871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac7cebdcdd35756c5e60649efaf9c73404be1163c0aa6785b56575d3a91d5195`  
		Last Modified: Mon, 22 Apr 2024 22:26:19 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:8c5237515cb51fc5bf2bba17bafb21d35101d69cc311750d460fbf22981a6a32
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.5 MB (142475270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddb44be8a4b00a22f71fd22110da989a49f7ef26b1f4cbafb0ae0281ccc768c6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 24 Apr 2024 04:06:51 GMT
ADD file:b6d26ef7cfc03fe202f7a5ac219566bc37f382ffadc9acdad685f2dd318cf0e4 in / 
# Wed, 24 Apr 2024 04:06:52 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:50:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 14:05:49 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 14:05:51 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 24 Apr 2024 14:06:20 GMT
ENV TELEGRAF_VERSION=1.30.2
# Wed, 24 Apr 2024 14:06:28 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 24 Apr 2024 14:06:29 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 24 Apr 2024 14:06:29 GMT
COPY file:3d723e9d10409fb06c7eaa4bbebe18017fc82dee6330d688adb684b64917f206 in /entrypoint.sh 
# Wed, 24 Apr 2024 14:06:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Apr 2024 14:06:30 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:80e84b3257949a283234599e3906626cfb4ff482d06fa4dc3eaf1dd36551dafa`  
		Last Modified: Wed, 24 Apr 2024 04:10:48 GMT  
		Size: 45.2 MB (45174994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52886721ea5a8a8bac2b197dccd42a74948b88bedcfe0fdf8b24e234c0a660d0`  
		Last Modified: Wed, 24 Apr 2024 05:02:39 GMT  
		Size: 22.0 MB (21953968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f49ff3c62cfa8259ba641f429364c1c98fb99aaace66ea71c110c0f3f6a2069b`  
		Last Modified: Wed, 24 Apr 2024 14:06:47 GMT  
		Size: 17.9 MB (17932145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcbf8d083657a1224c565a90b217288b841ff1f78db931977faaf6c32f8233ac`  
		Last Modified: Wed, 24 Apr 2024 14:06:42 GMT  
		Size: 1.8 KB (1814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:128efe4859364bc7e5609805398e7dedafefcbd75316d7dfb0bcb09212fa0430`  
		Last Modified: Wed, 24 Apr 2024 14:07:33 GMT  
		Size: 57.4 MB (57411726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68bf7594d0e12f0e1dd643d6d96bd53b36e7bfca8340cd1ecac6b069323c4a42`  
		Last Modified: Wed, 24 Apr 2024 14:07:23 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:25de4d9685c1049a17c469fc9d53b508d9e66493e02adde3b64292917fdc81a4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.7 MB (148699434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d75c995de34e0505e291b68efc64748d8b098a81d5c7d4fc4ba42caaa979ecb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:30 GMT
ADD file:07ae70ad05f39a24007b6bde4418c9934bc3865fe855dfcf62a44d8a30375739 in / 
# Wed, 24 Apr 2024 04:10:31 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 08:32:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 13:45:12 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 13:45:13 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 24 Apr 2024 13:45:38 GMT
ENV TELEGRAF_VERSION=1.30.2
# Wed, 24 Apr 2024 13:45:43 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 24 Apr 2024 13:45:44 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 24 Apr 2024 13:45:44 GMT
COPY file:3d723e9d10409fb06c7eaa4bbebe18017fc82dee6330d688adb684b64917f206 in /entrypoint.sh 
# Wed, 24 Apr 2024 13:45:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Apr 2024 13:45:44 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:60bdaf986dbe787297bb85c9f6a28d13ea7b9608b95206ef7ce6cdea50cd5505`  
		Last Modified: Wed, 24 Apr 2024 04:13:43 GMT  
		Size: 49.6 MB (49613341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e100ddc6b415c632410507293430c0fe6bb4228ab320ed59548c6dc030b4e4a`  
		Last Modified: Wed, 24 Apr 2024 08:41:28 GMT  
		Size: 23.6 MB (23586795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9935286a1f591251a12c663afdc2596adc4e8b91d91c60c7d53907023fed11a0`  
		Last Modified: Wed, 24 Apr 2024 13:46:02 GMT  
		Size: 19.1 MB (19077226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68421de5c53c46a30146ebc2684bda6aaf65e702e559619ca40243653b5623d8`  
		Last Modified: Wed, 24 Apr 2024 13:45:59 GMT  
		Size: 1.8 KB (1802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b16de5edc7a15e62e63cfdc108c79c735c6271c7c11e51887f8a368b6e0a8284`  
		Last Modified: Wed, 24 Apr 2024 13:46:36 GMT  
		Size: 56.4 MB (56419647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2660869aa1b2eea6577b68dd5606d242030b2f2635a4797574b712958232b86d`  
		Last Modified: Wed, 24 Apr 2024 13:46:29 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
