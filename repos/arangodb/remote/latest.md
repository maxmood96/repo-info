## `arangodb:latest`

```console
$ docker pull arangodb@sha256:5834757fc3544899eb412b876a0955ca301a24569caf61a43c77328fa60cacc3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `arangodb:latest` - linux; amd64

```console
$ docker pull arangodb@sha256:2928aea4e28141ed9e96a925bf7ec6d8266627d14649cf154291aaea86bbeb92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.3 MB (258314211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71981a3e1b2d0bbf2c226ccbab69990ece6c1d47d406dcccd75f6d52de650aab`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 01 Jul 2025 09:43:27 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Tue, 01 Jul 2025 09:43:27 GMT
ENV ARANGO_VERSION=3.12.5
# Tue, 01 Jul 2025 09:43:27 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/9c169fe900ff79790395784287bfa82f0dc0059375a34a2881b9b745c8efd42e/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3e_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Tue, 01 Jul 2025 09:43:27 GMT
ENV GLIBCXX_FORCE_NEW=1
# Tue, 01 Jul 2025 09:43:27 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Tue, 01 Jul 2025 09:43:27 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Tue, 01 Jul 2025 09:43:27 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 01 Jul 2025 09:43:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 01 Jul 2025 09:43:27 GMT
EXPOSE map[8529/tcp:{}]
# Tue, 01 Jul 2025 09:43:27 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c0ee9a5a889c2ace04c03100e8b029f758cc3f3f07c27ffe4e5a3e10fdcdc36`  
		Last Modified: Tue, 01 Jul 2025 21:13:31 GMT  
		Size: 254.7 MB (254669814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01245baf2d5bbf265b8bfb60757befe6a09059faacc4b9b6e986c36785ed13a1`  
		Last Modified: Tue, 01 Jul 2025 19:09:29 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae08dc040ed92dc856eb0ce24e09e3f9d8b9712cc240cda55390e8f2896bb3b`  
		Last Modified: Tue, 01 Jul 2025 19:09:29 GMT  
		Size: 2.0 KB (2012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:latest` - unknown; unknown

```console
$ docker pull arangodb@sha256:8b32ad10ffcc6b912fcb2a22bc140befe61417d3386854bc70a2c058d7743f86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **527.3 KB (527338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78b7ec5cf79da9a64b67209072d15054b42779567e8a112006854507509bc9df`

```dockerfile
```

-	Layers:
	-	`sha256:bc40f2866948a1a88879066be73c4bf0bc97acf60b843f57bbe31192abf52269`  
		Last Modified: Tue, 01 Jul 2025 21:13:19 GMT  
		Size: 512.8 KB (512800 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a56a1e95bac105415264d80ab8a5fb78b8bc6ca480b6e867e7ceaada08c7f3e`  
		Last Modified: Tue, 01 Jul 2025 21:13:20 GMT  
		Size: 14.5 KB (14538 bytes)  
		MIME: application/vnd.in-toto+json

### `arangodb:latest` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:bb2cfcbc81ebbbd4c6dcef0d981b0163fca049b2e72480c1ca7c17ab72fdc76e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.4 MB (257365264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca1ba9cb8576c2d5c551cc65eadce61c4a4d63cfe459b89099272ba499f7c624`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 10:13:28 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Thu, 26 Jun 2025 10:13:28 GMT
ENV ARANGO_VERSION=3.12.5
# Thu, 26 Jun 2025 10:13:28 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/9c169fe900ff79790395784287bfa82f0dc0059375a34a2881b9b745c8efd42e/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3e_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Thu, 26 Jun 2025 10:13:28 GMT
ENV GLIBCXX_FORCE_NEW=1
# Thu, 26 Jun 2025 10:13:28 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Thu, 26 Jun 2025 10:13:28 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Thu, 26 Jun 2025 10:13:28 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 26 Jun 2025 10:13:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 26 Jun 2025 10:13:28 GMT
EXPOSE map[8529/tcp:{}]
# Thu, 26 Jun 2025 10:13:28 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:547a06b378367053b090547e5d14ea85d1e91a64a068ab4c9f41e553deb78077`  
		Last Modified: Thu, 26 Jun 2025 21:18:31 GMT  
		Size: 253.4 MB (253370079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4aa1670916602c2e5e863b86324054cf2abb7655485993afbc11ce43675261f`  
		Last Modified: Thu, 26 Jun 2025 18:42:57 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1175ac9cddc3694aafd029e225e4fb18bf54ae13b9b865082ad795ad243a1954`  
		Last Modified: Thu, 26 Jun 2025 18:42:57 GMT  
		Size: 2.0 KB (2016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:latest` - unknown; unknown

```console
$ docker pull arangodb@sha256:485733aefcb95003e90537d5733ca5b700d9835f24578823be615398047318ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **678.1 KB (678066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfca49bf31b4108159e681e88bf889ef7fb4e0b94340eaa12364688f112b78d5`

```dockerfile
```

-	Layers:
	-	`sha256:4ea4d55ae702dd0614cd78ff8faeb0d38554e6c296a3f540b1cd429f53033bc0`  
		Last Modified: Thu, 26 Jun 2025 21:13:25 GMT  
		Size: 663.4 KB (663420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95756907dc560e6944330a2f0de2654266c8ccf33f9955058f5f7d8c52fb3daf`  
		Last Modified: Thu, 26 Jun 2025 21:13:26 GMT  
		Size: 14.6 KB (14646 bytes)  
		MIME: application/vnd.in-toto+json
