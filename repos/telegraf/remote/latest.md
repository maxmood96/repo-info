## `telegraf:latest`

```console
$ docker pull telegraf@sha256:9768f82ebf8bde6da0d61ba220c00161750740c3e322b507a5982b89bbfca99a
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
$ docker pull telegraf@sha256:3fc4238e808b2f478fc4b75ca20ad1591d7d8e4d00cd24c1849e06b0d7bb476d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.3 MB (175318286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cba2b198a419da73a31ba9e67d57290f8dcb68596fd0e81b78a75f63fddcc33f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:42:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:38:05 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:38:06 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 11 Jun 2026 02:38:10 GMT
ENV TELEGRAF_VERSION=1.39.0
# Thu, 11 Jun 2026 02:38:10 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Thu, 11 Jun 2026 02:38:10 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Thu, 11 Jun 2026 02:38:10 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jun 2026 02:38:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jun 2026 02:38:10 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:01cedcff86f879d042805360ecba268802bec3d8201484ff3ec54f4250a2d3b7`  
		Last Modified: Wed, 10 Jun 2026 23:39:39 GMT  
		Size: 48.5 MB (48502042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da31edd9efdb812e66d13819903973ea6b188d2e7358547676d33d1e3f706f2`  
		Last Modified: Thu, 11 Jun 2026 00:42:23 GMT  
		Size: 24.0 MB (24044000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e155aa599b08cfc50d0f771f6c9e59a26cc3db1ee8f23d96c752045946ebcb`  
		Last Modified: Thu, 11 Jun 2026 02:38:29 GMT  
		Size: 18.9 MB (18944395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7f40305f2528a0074d7b3653af61e0dabf428fc001c4f0ef4f673d8d00dcbf8`  
		Last Modified: Thu, 11 Jun 2026 02:38:28 GMT  
		Size: 5.1 KB (5070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10fe74ec8be4e76e3eeeaa5ce9e622028481c0ed8d57aa6be447a3bde9539cf2`  
		Last Modified: Thu, 11 Jun 2026 02:38:31 GMT  
		Size: 83.8 MB (83822154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b36e074ab3ae61fe91559fea6042fff3bf206c18d93dd5a8b48c3a2388b2217`  
		Last Modified: Thu, 11 Jun 2026 02:38:28 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:cd95848d5b140458c457b030ae76b9f962124f03bd360f55355f8ceccf38ab4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6687666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97ab420b7b4f8d15cba4ec1c2fb5a15733b264a6bcff0b85758504baf20d4c9d`

```dockerfile
```

-	Layers:
	-	`sha256:beef73a3089eafad7c4e32aed5edcf8380afa58610e43ecdf90a802ad49c1ba3`  
		Last Modified: Thu, 11 Jun 2026 02:38:29 GMT  
		Size: 6.7 MB (6672937 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b4cf003c03def45113a2bed2a8208f28f824177d46f372be4ded5526487f05a`  
		Last Modified: Thu, 11 Jun 2026 02:38:28 GMT  
		Size: 14.7 KB (14729 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:a946077d5018834e7983558f2a0a57f000252e11c0900f6bbade39b5a9326138
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.6 MB (161564792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0331c7b809a0c64ebcdcd52942423b4c1a6a408fc06433191d4e7b01807fcbd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 01:23:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 03:12:51 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 03:12:51 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 11 Jun 2026 03:12:57 GMT
ENV TELEGRAF_VERSION=1.39.0
# Thu, 11 Jun 2026 03:12:57 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Thu, 11 Jun 2026 03:12:57 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Thu, 11 Jun 2026 03:12:57 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jun 2026 03:12:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jun 2026 03:12:57 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c0213091aa87e4be7caed06dd364889c231dab5ba50fa1e54365eb7a94390261`  
		Last Modified: Wed, 10 Jun 2026 23:39:46 GMT  
		Size: 44.2 MB (44208065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d14356188705148a948907491c78974967557826c6ca92209148b3bc14f0f659`  
		Last Modified: Thu, 11 Jun 2026 01:23:38 GMT  
		Size: 21.9 MB (21949873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80941b0bdd88cb14fce09cd860981822c6590d738dd60fa2b425ad1a2429293d`  
		Last Modified: Thu, 11 Jun 2026 03:13:15 GMT  
		Size: 17.7 MB (17699817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9b6c1fafb4b14de088e98dca0de3494f44b322e5b325eafc52eec89ddc5148`  
		Last Modified: Thu, 11 Jun 2026 03:13:14 GMT  
		Size: 5.1 KB (5056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9141dff73825ba6ee195b24a91285533c2cad6d58c0626cfcbd901eafd72b97`  
		Last Modified: Thu, 11 Jun 2026 03:13:17 GMT  
		Size: 77.7 MB (77701357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4875f91dfac36b7631c83f84ec7dff018503073edc88c769230e2fa1c6e5467`  
		Last Modified: Thu, 11 Jun 2026 03:13:13 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:0487b9099eff11da70a8440c42beb10e2ba249c22ad6fb3a433944557e112fb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6682368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff9095f5ab3dc9b58e92061b8b9f1af712195195681919d0b8dd34df8ce73f59`

```dockerfile
```

-	Layers:
	-	`sha256:883ba0a7487f08ce93931197cc951f75d91ed7302d25f321b397295cb37fa629`  
		Last Modified: Thu, 11 Jun 2026 03:13:14 GMT  
		Size: 6.7 MB (6667542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6087deec867efbcf573afe33841bba228436e08b33510f1eda0178b058b8dc24`  
		Last Modified: Thu, 11 Jun 2026 03:13:14 GMT  
		Size: 14.8 KB (14826 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:ef03e3f7e60c80c324d644e62848925dabd58fde52b7bede56a9df33c4138150
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.6 MB (165642228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e803603c69c0fec78a586496a6ecc0819c8e3280219e4cfa6a92181c5958afae`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:43:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:37:33 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:37:34 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 11 Jun 2026 02:38:09 GMT
ENV TELEGRAF_VERSION=1.39.0
# Thu, 11 Jun 2026 02:38:09 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Thu, 11 Jun 2026 02:38:09 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Thu, 11 Jun 2026 02:38:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jun 2026 02:38:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jun 2026 02:38:09 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c847f328095fb083f4a22895b90fe4226efa6458ac57362b64b6e5d99da9e4a3`  
		Last Modified: Wed, 10 Jun 2026 23:39:28 GMT  
		Size: 48.4 MB (48389016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f511b4c80a6e453785fbcd573c1bf1cb986c4e8d43ed4500ad1ac9a4719762b`  
		Last Modified: Thu, 11 Jun 2026 00:43:56 GMT  
		Size: 23.6 MB (23613296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c190ef3f5f7acc6d44552bd3c4080c3a0fe6a2b8c594caff252a7a6d1b89a523`  
		Last Modified: Thu, 11 Jun 2026 02:37:55 GMT  
		Size: 18.9 MB (18885883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f24b9de6d86f6333b5aa1983c1dd0a8f6873a5a2904c22c512d14cbd25b77c`  
		Last Modified: Thu, 11 Jun 2026 02:37:55 GMT  
		Size: 5.1 KB (5071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ae3a233fa6f07584fe61e4bb99d85f21204734e79571844baae03bfab53654`  
		Last Modified: Thu, 11 Jun 2026 02:38:28 GMT  
		Size: 74.7 MB (74748337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a94bad00e15d9a51745fd11cdda66763215b62892a220dd25d0c9c2daee0120c`  
		Last Modified: Thu, 11 Jun 2026 02:38:25 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:d3da96f26730a480bde408c681552dc264b705778d2808b7f4cac2b0012caaf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6688475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd605b571f78407a533a0a4ce989a44613ce9da57de9dbe252d1d75730603ec6`

```dockerfile
```

-	Layers:
	-	`sha256:325a4ab33a42d976c41276df893b8a6fac1ffb11c32e74d323a73300ffcab816`  
		Last Modified: Thu, 11 Jun 2026 02:38:25 GMT  
		Size: 6.7 MB (6673625 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edc92bac93d6fe676f799a5b64caa5c8dd2703a51b4e1427264c7e693404085e`  
		Last Modified: Thu, 11 Jun 2026 02:38:25 GMT  
		Size: 14.8 KB (14850 bytes)  
		MIME: application/vnd.in-toto+json
