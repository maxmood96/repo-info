## `chronograf:latest`

```console
$ docker pull chronograf@sha256:0f4001a8ea798124c062d6a5129a5a8727b7e039ec080f7900794e357511a191
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `chronograf:latest` - linux; amd64

```console
$ docker pull chronograf@sha256:cbb2398ca1e9c1e79905f76a6f508c0b84e124ed19d8bd1ef329113df6bd0554
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.2 MB (84245436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ef430dd9bd942ea971170a9ad41a7b86bf2b0bd54963f64e172414e8bbf7b6a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.10.5
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1224e7e2d3fcfa467dc4f217326c057f4f2dd7300e13ef8f9e857ce39d3b4a1a`  
		Last Modified: Tue, 12 Nov 2024 02:38:20 GMT  
		Size: 7.9 MB (7875383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:156341f7966c50570025c0aa511f08d25d6323a659a42aed5dbf0d667f59476a`  
		Last Modified: Tue, 12 Nov 2024 02:38:20 GMT  
		Size: 47.2 MB (47217593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc833227a91630f06fdbd4aa78c70728725f847e7108c30819c0dd7b1bcc2f1`  
		Last Modified: Tue, 12 Nov 2024 02:38:19 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:942d7292f5707350b55e75b6962c10f687a2f79cd6897f52184d0d756f3640af`  
		Last Modified: Tue, 12 Nov 2024 02:38:20 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e59b128af6ad42b6a2e4237a81330a24126fa56928cb1282247f5a0b2e934cce`  
		Last Modified: Tue, 12 Nov 2024 02:38:20 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:d283d9166d23e08f8f2ecab79a9506abca9aca59180582cf53a41af1716e8570
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2722905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dff9e10e6a0907fdc037209f268bd74095409b257480933f04b1cad3729d68f`

```dockerfile
```

-	Layers:
	-	`sha256:3e81168bed413e125218f95a0a4120c7164a7f95a704ffc312fa47035416659c`  
		Last Modified: Tue, 12 Nov 2024 02:38:20 GMT  
		Size: 2.7 MB (2706777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8da14de2590a125267c353c750cc1c061c345a17e9a5da32b3651a9e5dc1c2ec`  
		Last Modified: Tue, 12 Nov 2024 02:38:19 GMT  
		Size: 16.1 KB (16128 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:latest` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:13a78f4c253093cf30fca5c89c1bb696e1fc682c1b7810e70e5a4c3ed0cc5151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75516412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d71adce3a94e5289bac0d13f5cc4efb87d068f50d800592bc297e2793cbe9ea`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:e76e8ba7ebca0b1dcaec16ad1e863ab59c7e155f0b95ba46f5543e418a904b35 in / 
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.10.5
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:d6319e551f4eae5cadf245338228c7b7cbad94a77c481a88ccbffef7b89f0aee`  
		Last Modified: Thu, 17 Oct 2024 03:06:55 GMT  
		Size: 24.7 MB (24718197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:907a2e66a49258f3d38a009ec8390c0ca30e9b21e10c1f97f033935a3cc5547d`  
		Last Modified: Thu, 17 Oct 2024 06:28:46 GMT  
		Size: 6.5 MB (6497599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab246a3e9d45eb0ec1e5d6429010eebe6b5030c07dbb87501a3ceca74ea685b9`  
		Last Modified: Thu, 17 Oct 2024 06:28:47 GMT  
		Size: 44.3 MB (44276153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6311c1ec06eb271b214b2fb3b0ec782a808c8ccbf31c6753f73123807ef5811`  
		Last Modified: Thu, 17 Oct 2024 06:28:45 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e6079489fc1564886a6fb52e0420b2c1478c533f5d728c5f252a9020d11ff0a`  
		Last Modified: Thu, 17 Oct 2024 06:28:47 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f8925067ffa8213682865f92f9c8e961b3a242bf92478a328aa37bafa4db9b`  
		Last Modified: Thu, 17 Oct 2024 06:28:47 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:4d5d473389d12da9d271eb185b6a74cb3f4555b5f0067cca46a140fa3143c38c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2709303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:837b3ca99f4b4f58ae00c768cdda7420b29c4d4adbb04fe379004c82e8e8019a`

```dockerfile
```

-	Layers:
	-	`sha256:0bc9dce96a65ba948929d290d404f8baa6920851fe61442b3dddea26a887d674`  
		Last Modified: Thu, 17 Oct 2024 06:28:46 GMT  
		Size: 2.7 MB (2693256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6257c8555aefbf425ff0fc7ba80af9cfaff204b57d960f0c1ed989a1ea96928`  
		Last Modified: Thu, 17 Oct 2024 06:28:46 GMT  
		Size: 16.0 KB (16047 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:latest` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:55b50dea2f2137ce54f443d25b2abfeae47947ee823b2f08388d6eda47d37d8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.8 MB (81804433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22992893a7f71a7317d6d6a37c09a42bd342530c32f54b834b877cf5e2c5ab0c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.10.5
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5311845117483a02d47c2a837750ed149b17f6ad45451557d3edf3b2361b65d1`  
		Last Modified: Tue, 12 Nov 2024 11:20:18 GMT  
		Size: 7.7 MB (7652059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9f1f751938fc31cf6a008145a362d6ef94697cef76dd2dcd3a8bb9c969ba5f5`  
		Last Modified: Tue, 12 Nov 2024 11:20:19 GMT  
		Size: 45.0 MB (44970549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fa6316747afbf579f3ace66f98703019df3b8b3d7083660d7e299b89205fc7b`  
		Last Modified: Tue, 12 Nov 2024 11:20:18 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ad95dbffe5e0b91bcdb9f70a444a19e3b49b1f65366caee2370468e451a8ff`  
		Last Modified: Tue, 12 Nov 2024 11:20:18 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:522a008c121d0b587cccc212b8a01b87d0893dd790681b545ce2777b6031c31f`  
		Last Modified: Tue, 12 Nov 2024 11:20:19 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:8005aae06ed87a042209bcd22fd86c390c027dfefd1ab385657eb9c4ff90b1ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2723284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a57bfeb1040a95763cafa6296c548fbc9a7c9d83b29c2a572fdd51e3e6aa28ce`

```dockerfile
```

-	Layers:
	-	`sha256:519a1a88095896e326f6589cb0448391ad985d186bae96a9b24df79476d03244`  
		Last Modified: Tue, 12 Nov 2024 11:20:18 GMT  
		Size: 2.7 MB (2707049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6e694a5a62286326bdb76d6c68673eb2b6e170f2c7e26eb255c0224ddbc61be`  
		Last Modified: Tue, 12 Nov 2024 11:20:18 GMT  
		Size: 16.2 KB (16235 bytes)  
		MIME: application/vnd.in-toto+json
