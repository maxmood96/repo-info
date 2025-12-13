## `kapacitor:latest`

```console
$ docker pull kapacitor@sha256:7fa702d2444080c86ba6b0733286a7324800b4c0faa3177349b4852d7f93602a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:latest` - linux; amd64

```console
$ docker pull kapacitor@sha256:ad424b6437336383d6709f715fcc4d07447a25631933fff8ebf822c8b822ccc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.1 MB (173104505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47fcb0d2a2b24d7a2375a04baa29202f7c1dd9161e1024061225fc72f3b24caa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:09:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:28:01 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Fri, 14 Nov 2025 00:28:08 GMT
ENV KAPACITOR_VERSION=1.8.2
# Fri, 14 Nov 2025 00:28:08 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Fri, 14 Nov 2025 00:28:08 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Fri, 14 Nov 2025 00:28:08 GMT
EXPOSE map[9092/tcp:{}]
# Fri, 14 Nov 2025 00:28:08 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 14 Nov 2025 00:28:08 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 14 Nov 2025 00:28:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 14 Nov 2025 00:28:08 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e9c2d709d1a081127422a39a26861612ac4b73362a9abfb7ce643122e4082a`  
		Last Modified: Thu, 13 Nov 2025 23:09:24 GMT  
		Size: 7.1 MB (7106219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c7135dbac77e480e19f2fab49d6bf449a7b00e25043f30204f2c35cbaf2081e`  
		Last Modified: Fri, 14 Nov 2025 00:28:35 GMT  
		Size: 48.2 MB (48248227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4667606aa22066eb1ead38518f235c333ee2336fb3ca2ac1e9be16644ca7e4cd`  
		Last Modified: Fri, 14 Nov 2025 00:28:41 GMT  
		Size: 88.2 MB (88212738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82416f38ec3797f036f93179be2ce2564f4204507898f04753b75730f39d8da1`  
		Last Modified: Fri, 14 Nov 2025 00:28:31 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de306879312a1e10fffc2828bfc33198774cbaaf6d943b4ff63f9ffa63c7a639`  
		Last Modified: Fri, 14 Nov 2025 00:28:32 GMT  
		Size: 297.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:latest` - unknown; unknown

```console
$ docker pull kapacitor@sha256:a7da07e90eadc8945c1c0cf7649e29a39ab734e3a29ad19d3018ec47d2c599e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3746289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a54ded414376942e7256e72a433b9d8afcb21ae4aecc958a903df8836ba5003`

```dockerfile
```

-	Layers:
	-	`sha256:4cba04e58c70efe1eba618345ae547556183fc88c902756df7a4c8c3928c2438`  
		Last Modified: Fri, 14 Nov 2025 02:21:57 GMT  
		Size: 3.7 MB (3731269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f07e8b3b981f40dab492441333de3d022e7c2be22df664e320c2b50065dbe332`  
		Last Modified: Fri, 14 Nov 2025 02:21:58 GMT  
		Size: 15.0 KB (15020 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:latest` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:d0d87f6e0e8ae3377d4dd02dde6bbbcfedbda40aacf90bdb018ff091f604e663
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.8 MB (162750022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55d05fb9a6cec856b762b1711ec4b5346c0d92050196a6152c416247d87409f2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:09:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:28:20 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Fri, 14 Nov 2025 00:28:26 GMT
ENV KAPACITOR_VERSION=1.8.2
# Fri, 14 Nov 2025 00:28:26 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Fri, 14 Nov 2025 00:28:26 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Fri, 14 Nov 2025 00:28:26 GMT
EXPOSE map[9092/tcp:{}]
# Fri, 14 Nov 2025 00:28:26 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 14 Nov 2025 00:28:26 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 14 Nov 2025 00:28:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 14 Nov 2025 00:28:26 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e799c76d7a2425b1efa4aab18a6ff0211a5844ff8737a1e027e934d92c1ac935`  
		Last Modified: Thu, 13 Nov 2025 23:09:14 GMT  
		Size: 7.1 MB (7052496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc514c00b5880177c45acb158773e3e0427cbf47b9e3ec5fe3976be52704a5a7`  
		Last Modified: Fri, 14 Nov 2025 00:28:52 GMT  
		Size: 46.3 MB (46303484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9e4b28f4c70b491bc425ae0c0b8fc849fc3a59ff25d3efa2fb9cf1a9bc76e6`  
		Last Modified: Fri, 14 Nov 2025 00:28:54 GMT  
		Size: 82.0 MB (82009642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df04f27e6295adef6bb6401f0ec49a56d23f939eb1e2cec9249cc69807c93d9c`  
		Last Modified: Fri, 14 Nov 2025 00:28:48 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faba64dc4b68645941b6e163791183152612fa0ebc92fee387fd4660750cabaa`  
		Last Modified: Fri, 14 Nov 2025 00:28:48 GMT  
		Size: 298.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:latest` - unknown; unknown

```console
$ docker pull kapacitor@sha256:01cc88792432f43c356679ae274fef28b207b3c1240b69c9dc3fe010ad2ff4ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3745870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:738e95c87a147a28fed5df5662afaf5075e693a74b2b61815a98c2a2f78d7286`

```dockerfile
```

-	Layers:
	-	`sha256:a39870c15d12b577e34cfbba53326926f1c47027f4ff66efd70517a8a6e9b525`  
		Last Modified: Fri, 14 Nov 2025 02:22:03 GMT  
		Size: 3.7 MB (3730743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59e700bf823a01ee7b340e763219eb84fc053accb5b66c1ea64c45a2553bb236`  
		Last Modified: Fri, 14 Nov 2025 02:22:03 GMT  
		Size: 15.1 KB (15127 bytes)  
		MIME: application/vnd.in-toto+json
