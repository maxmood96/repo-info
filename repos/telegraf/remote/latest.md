## `telegraf:latest`

```console
$ docker pull telegraf@sha256:f0870a1e3faa0504fad06751d662e082baf026451b01c7bf58585ddda2739a01
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:latest` - linux; amd64

```console
$ docker pull telegraf@sha256:f9c42b8ab8d1a65ca86c3bfcb860f9e07b46c6df37b09181645c3f681dd71b76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.3 MB (175318400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b36fd5af2d996be82c68fd752646216c0514960d02c1812c0750a936e3e2d427`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 01:41:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 02:43:54 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 02:43:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 24 Jun 2026 02:43:58 GMT
ENV TELEGRAF_VERSION=1.39.0
# Wed, 24 Jun 2026 02:43:58 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Wed, 24 Jun 2026 02:43:58 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Wed, 24 Jun 2026 02:43:58 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 24 Jun 2026 02:43:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Jun 2026 02:43:58 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:425befdf76e52426879d2abe42093a00dca59a893e7b4fa2a7679b0180b71d4b`  
		Last Modified: Wed, 24 Jun 2026 00:27:40 GMT  
		Size: 48.5 MB (48502210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4fd7bf6f6036613e20f62549df75ed694b99118002358bea5a81baf3929d1ff`  
		Last Modified: Wed, 24 Jun 2026 01:41:33 GMT  
		Size: 24.0 MB (24044046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94ef38ee29d7f9ad90b26a9599253b6cbe3723c272ddeb5462cae4694855b8b4`  
		Last Modified: Wed, 24 Jun 2026 02:44:19 GMT  
		Size: 18.9 MB (18944340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7471fdfd03d0654197c4206733cd704520659ed52d49cf4b91a53dc77f125b`  
		Last Modified: Wed, 24 Jun 2026 02:44:18 GMT  
		Size: 5.1 KB (5056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9749bf8de53fafdfb75e7b3690151a2aa32e8e09a5e50fa9c465e0fc1c24b70`  
		Last Modified: Wed, 24 Jun 2026 02:44:20 GMT  
		Size: 83.8 MB (83822123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dc442a7db01992ffe288d3bf5336ab36885be5399ec32aa998413717e1946bd`  
		Last Modified: Wed, 24 Jun 2026 02:44:18 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:cf184f166bed8302e55bc83bb844ea827c61016b30106f79fae008c78b3d134a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6687666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab442fa0427c83b5b557f65c7a9f6f79a58178967588aaa3e5a41df4d2d73839`

```dockerfile
```

-	Layers:
	-	`sha256:c0d9e061c5671c946b319f23843768b4e00cf9fb19a6c7a686acc623a091de38`  
		Last Modified: Wed, 24 Jun 2026 02:44:18 GMT  
		Size: 6.7 MB (6672937 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4aa9cc870961e69384940f2c91b6687de79c3cb6f7d32711c4dae2cf4adfb36c`  
		Last Modified: Wed, 24 Jun 2026 02:44:18 GMT  
		Size: 14.7 KB (14729 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:0664da2c8ceb0f3d96a4d8187e7e5eda8db5bb54578758c38cb657298e07053a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.6 MB (161564827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeb0112bf4815527a917553ff2a5efbd0043de3b2f7559cb74af65ea46f3f4f8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:22:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 04:09:54 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 04:09:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 24 Jun 2026 04:10:01 GMT
ENV TELEGRAF_VERSION=1.39.0
# Wed, 24 Jun 2026 04:10:01 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Wed, 24 Jun 2026 04:10:01 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Wed, 24 Jun 2026 04:10:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 24 Jun 2026 04:10:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Jun 2026 04:10:01 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:3622debffba3838b917703fb6dd9c161a4d93d9fd97c61d3e8400a2245f93c67`  
		Last Modified: Wed, 24 Jun 2026 00:27:30 GMT  
		Size: 44.2 MB (44208145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d0df8de55f365d832099cabf27409104999d59b26292d91202ca6e160c4b513`  
		Last Modified: Wed, 24 Jun 2026 02:22:52 GMT  
		Size: 21.9 MB (21949935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a8a4eb9ec7a50c6472c9ae430d62d6b15e7b83a12a5bf3088b618f55466227f`  
		Last Modified: Wed, 24 Jun 2026 04:10:19 GMT  
		Size: 17.7 MB (17699692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b92ea1626c4eb8d2fc134366d546a9667c125f62127318217255de87a7b1cc9`  
		Last Modified: Wed, 24 Jun 2026 04:10:18 GMT  
		Size: 5.1 KB (5052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d1b0fc52b69aa258581e73ca27f984b95b797e9f6c86a100a81b3af4e15d72`  
		Last Modified: Wed, 24 Jun 2026 04:10:20 GMT  
		Size: 77.7 MB (77701378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e5cbe0a6e378522eafb86c405494b771441646c9b9f0d13858b2722e8f7ccc2`  
		Last Modified: Wed, 24 Jun 2026 04:10:18 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:9101252b685ea71de23c3b258fa02912aa2f046ec85196960899813143dc7d9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6682369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:226bcfa3d033e69534b17db231e59b01f2b4d56e1531109a3bbf9fc7423e9341`

```dockerfile
```

-	Layers:
	-	`sha256:6198665174b0e5f02af9759193658a77f7c0f2a83e786d43001fa2790c530d1f`  
		Last Modified: Wed, 24 Jun 2026 04:10:18 GMT  
		Size: 6.7 MB (6667542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76b23661ddb0d404706d9b689dfa67700e9203a4230909c673a864de61afdf4a`  
		Last Modified: Wed, 24 Jun 2026 04:10:18 GMT  
		Size: 14.8 KB (14827 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:baacbcb9d8e701710fca488ab537dd34bff9b464d9c26dbd82606bfa722a3869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.6 MB (165642469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d71b9f2500351b590f99e800f43d06cf527968813aa99ea4aac4de106a82d405`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 01:44:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 02:49:56 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 02:49:56 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 24 Jun 2026 02:50:00 GMT
ENV TELEGRAF_VERSION=1.39.0
# Wed, 24 Jun 2026 02:50:00 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Wed, 24 Jun 2026 02:50:00 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Wed, 24 Jun 2026 02:50:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 24 Jun 2026 02:50:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Jun 2026 02:50:00 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:0fb1189398e2e4b474d43aac6502510d0da0318e70137a377c21087f198814db`  
		Last Modified: Wed, 24 Jun 2026 00:27:19 GMT  
		Size: 48.4 MB (48389201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ebca214f1a4b66acfdb0bd20aa3ee139d1747885ef4b0f3d07aa2a68459230`  
		Last Modified: Wed, 24 Jun 2026 01:44:48 GMT  
		Size: 23.6 MB (23613316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a198553af118f5fe585b2f68758bd12f9c4596b405148af4e6fbe08316adffec`  
		Last Modified: Wed, 24 Jun 2026 02:50:19 GMT  
		Size: 18.9 MB (18885931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4486cfbc0ef87efb9258302403db91c4e087a4a5fa6e0bf7003a3db34a4cb4e9`  
		Last Modified: Wed, 24 Jun 2026 02:50:18 GMT  
		Size: 5.1 KB (5055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c1e5208a79930a97a6d722801d49a918d4d8227f0db70cecb4855c2125ae669`  
		Last Modified: Wed, 24 Jun 2026 02:50:21 GMT  
		Size: 74.7 MB (74748341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b528cbfb3d9e2b9483e8494a83ecfd3d02d3ba1ae5f3562e2d1d1910203704a`  
		Last Modified: Wed, 24 Jun 2026 02:50:18 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:1de18f66993d9fdf82afeee59a2fc368b9e91767ebb2d3c9cb60c67280b58baf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6688476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f134593394be4d4e92e0658ebaea2a630e95a0395039c19a1d796da0aeaae34`

```dockerfile
```

-	Layers:
	-	`sha256:404c5265660780dc8e6006fdcb87a113dbf687b6c4822b4f0087aeb38b549da4`  
		Last Modified: Wed, 24 Jun 2026 02:50:18 GMT  
		Size: 6.7 MB (6673625 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21c627d94f51a2255f5cffd46c1001c62dbec25c9d219a7061ef177c523aef0d`  
		Last Modified: Wed, 24 Jun 2026 02:50:18 GMT  
		Size: 14.9 KB (14851 bytes)  
		MIME: application/vnd.in-toto+json
