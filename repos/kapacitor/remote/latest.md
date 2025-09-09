## `kapacitor:latest`

```console
$ docker pull kapacitor@sha256:151a9b8048ad32bb0f951f52e6b234585a25d123086b09eef6a62017173a30e5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:latest` - linux; amd64

```console
$ docker pull kapacitor@sha256:83a283e3f8ff5a85c07ec7f0a5e8a92034d4a2697e81c618c56f63b7ccf689fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.3 MB (171295058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0393e7fff8b0e88248763ce600b71fca1725f618c64b8bd44e70451a1913b6d2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Sep 2025 19:01:34 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Mon, 08 Sep 2025 19:01:34 GMT
ENV KAPACITOR_VERSION=1.8.1
# Mon, 08 Sep 2025 19:01:34 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 08 Sep 2025 19:01:34 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Mon, 08 Sep 2025 19:01:34 GMT
EXPOSE map[9092/tcp:{}]
# Mon, 08 Sep 2025 19:01:34 GMT
VOLUME [/var/lib/kapacitor]
# Mon, 08 Sep 2025 19:01:34 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 08 Sep 2025 19:01:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Sep 2025 19:01:34 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6828c7dda7e5e4b9c82ddb483379bdc791aa9b7cecdce2c883c603e7806ea9a`  
		Last Modified: Mon, 01 Sep 2025 23:07:56 GMT  
		Size: 7.1 MB (7106278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:675f4a535b891f2377c1a7a7b82555cec5aa36a8758c32fdaeab89e5b8fce6a5`  
		Last Modified: Tue, 09 Sep 2025 01:22:50 GMT  
		Size: 46.4 MB (46434426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf4d47d85c84fe9a8df9d0d24486bc7b366c7cd1bdb265a253a84d78151ee5c`  
		Last Modified: Tue, 09 Sep 2025 01:22:52 GMT  
		Size: 88.2 MB (88216894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7e8a2ae4f47c8852d0ade605f12fc1d6411342ca5b085e22e3a9a214ab12ae2`  
		Last Modified: Mon, 08 Sep 2025 22:52:41 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2589272d22bcea7dd2494c47fc31ca9001d9eaf6f99dc23e1db1f6fd1b4733a`  
		Last Modified: Mon, 08 Sep 2025 22:52:44 GMT  
		Size: 298.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:latest` - unknown; unknown

```console
$ docker pull kapacitor@sha256:ded0e700c3354b5e8aabe784d4a3f73b0f8cbe2f8748a5af1212228d7a2c36dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3746332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4b5d67a8b6f89716c1688e383bdbbc3937d14b57111dadc0a054b4fb7621a48`

```dockerfile
```

-	Layers:
	-	`sha256:8886a40144a1ca91d92baaccd77853c3e5fcd4fadaa08067c09e3f40a098467d`  
		Last Modified: Tue, 09 Sep 2025 01:21:19 GMT  
		Size: 3.7 MB (3731269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d125f5ce7f5c1080da6e9cf1d23aac50081110acab6d6c17aa1bba2f7aa34a5`  
		Last Modified: Tue, 09 Sep 2025 01:21:21 GMT  
		Size: 15.1 KB (15063 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:latest` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:34100f6f7977f8d021357b1a2ca36c97211c65825875426ab734dcc921ee64bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.9 MB (159861919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ee2588efd929c3449bbaf353507e5bf4badc827ade6b0d888dfd248b15b858c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
ENV KAPACITOR_VERSION=1.8.0
# Tue, 08 Jul 2025 13:10:35 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 08 Jul 2025 13:10:35 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 08 Jul 2025 13:10:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 08 Jul 2025 13:10:35 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:573b56f55094f2d14930c686b1a46091f6f5d62cadec0da94af57c5297b32867`  
		Last Modified: Tue, 02 Sep 2025 01:18:59 GMT  
		Size: 7.1 MB (7051940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9638ee345f265593b563464cf568a673d0e98db70e231aef56afc0c86d6f286`  
		Last Modified: Tue, 02 Sep 2025 04:52:49 GMT  
		Size: 44.0 MB (43984242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59f402fe2a98fccc20b255c74fc100f94277b4d06d76463132c72f7dafe4354c`  
		Last Modified: Tue, 02 Sep 2025 04:53:16 GMT  
		Size: 81.5 MB (81463748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39af266d7e47648a14fdb6b8830ffa7be8c484cc139c85f859afe809596f8a46`  
		Last Modified: Tue, 02 Sep 2025 04:53:11 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fde9ad70a06bb672ecbda12db9678a6169991c4b47437bcad91e8534b1da785`  
		Last Modified: Tue, 02 Sep 2025 04:53:11 GMT  
		Size: 296.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:latest` - unknown; unknown

```console
$ docker pull kapacitor@sha256:cfd4dedb60a41e390dfc9b85f77931871b8c969d9b9f2c66a2e4cd9b4710abe7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3745913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c52a169f7adcf5777253e75e49451f8f22ed2296184905887b4c37b3bbf0b9e8`

```dockerfile
```

-	Layers:
	-	`sha256:118e2379b18bbc6b19ac0580208229b47d3983d8e258bab1ab4daba884071bc1`  
		Last Modified: Tue, 02 Sep 2025 07:21:27 GMT  
		Size: 3.7 MB (3730743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5c7c8d6d7b816b935b3174bb953a63e4d5a9b1a5d8acc1a2861a6a198083d06`  
		Last Modified: Tue, 02 Sep 2025 07:21:27 GMT  
		Size: 15.2 KB (15170 bytes)  
		MIME: application/vnd.in-toto+json
