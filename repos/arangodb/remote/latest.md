## `arangodb:latest`

```console
$ docker pull arangodb@sha256:81dc1e0f812b5439f225b9fbdb6e0ac2ca583cf5a81aa82d4387e3a8a3de9571
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `arangodb:latest` - linux; amd64

```console
$ docker pull arangodb@sha256:7b96d84d2092ba9b5d137516c4de4ed06931740af24c67226b67999ba5ec05b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.4 MB (260350781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f253059f966c33466c579bf9e0beb1795322040da9411ac40861240ff96c76f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:43 GMT
ADD alpine-minirootfs-3.21.6-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:43 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:14:17 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Wed, 28 Jan 2026 02:14:17 GMT
ENV ARANGO_VERSION=3.12.7.1
# Wed, 28 Jan 2026 02:14:17 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/9c169fe900ff79790395784287bfa82f0dc0059375a34a2881b9b745c8efd42e/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3e_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Wed, 28 Jan 2026 02:14:17 GMT
ENV GLIBCXX_FORCE_NEW=1
# Wed, 28 Jan 2026 02:14:17 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Wed, 28 Jan 2026 02:14:17 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Wed, 28 Jan 2026 02:14:17 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 02:14:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:14:17 GMT
EXPOSE map[8529/tcp:{}]
# Wed, 28 Jan 2026 02:14:17 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:bc1da058f299723f8258c5a82dd007d1dd72e275087b726d5e1be5ef6198f286`  
		Last Modified: Wed, 28 Jan 2026 01:18:49 GMT  
		Size: 3.6 MB (3643742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e55508947b0557f86c5c646ad05b3ae78cc9940b21dc382fd85500a2ba1a4cc`  
		Last Modified: Wed, 28 Jan 2026 02:14:50 GMT  
		Size: 256.7 MB (256704884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:976a71614c82f23570733696b49d7d0ad7fe9eed1aa7c574b349488d47c2e5a5`  
		Last Modified: Wed, 28 Jan 2026 02:14:44 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d85bbd359ab00a8d060df68abadc9af9bb02593a2a1c168e21fbbf4ba104589`  
		Last Modified: Wed, 28 Jan 2026 02:14:44 GMT  
		Size: 2.0 KB (2015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:latest` - unknown; unknown

```console
$ docker pull arangodb@sha256:40b42af06433cf228285d7c034be690cd5b243309bac8f5118e6849a4dca9728
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **529.8 KB (529841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18eedcb7c55d7325b3b7ab5e41d7bca0a6feb0843ff4259717da9baab395b5c0`

```dockerfile
```

-	Layers:
	-	`sha256:87ef88a63465bbdc570f44381a9bd4f18037b7f394a90737ee25e8af9a95b431`  
		Last Modified: Wed, 28 Jan 2026 02:14:44 GMT  
		Size: 515.0 KB (515010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66f03b38e66d8a9f02f3000400aceb06390f1204b316301fec2dc061e9d9ca03`  
		Last Modified: Wed, 28 Jan 2026 02:14:44 GMT  
		Size: 14.8 KB (14831 bytes)  
		MIME: application/vnd.in-toto+json

### `arangodb:latest` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:2d6b22ae68676da98b8840e31c537236df2528b2c3a193feb223ac648d63cbb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.3 MB (259309876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3f6a798d4b0ef671bbea78d49fb62a6f308bf7f7cced7c9e666e62958955e40`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:07 GMT
ADD alpine-minirootfs-3.21.6-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:07 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:15:05 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Wed, 28 Jan 2026 02:15:05 GMT
ENV ARANGO_VERSION=3.12.7.1
# Wed, 28 Jan 2026 02:15:05 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/9c169fe900ff79790395784287bfa82f0dc0059375a34a2881b9b745c8efd42e/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3e_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg # buildkit
# Wed, 28 Jan 2026 02:15:05 GMT
ENV GLIBCXX_FORCE_NEW=1
# Wed, 28 Jan 2026 02:15:05 GMT
RUN echo "UTC" > /etc/timezone # buildkit
# Wed, 28 Jan 2026 02:15:05 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Wed, 28 Jan 2026 02:15:05 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 02:15:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:15:05 GMT
EXPOSE map[8529/tcp:{}]
# Wed, 28 Jan 2026 02:15:05 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:a447a5de8f4eb4a987d81c0afa14d459cc714599c020c08f45fafa9c6c904b30`  
		Last Modified: Wed, 28 Jan 2026 01:18:13 GMT  
		Size: 4.0 MB (3992880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f15f5b69a17ebed1a2c332d60abfdcb2dc29fcdadcc37790cf5f3b13fc3ee649`  
		Last Modified: Wed, 28 Jan 2026 02:15:39 GMT  
		Size: 255.3 MB (255314842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2fe7c40899f221c01952dd9eebc0f27902b1413dc72bf4ba49b08f71d244c34`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16d1b061900892dfc9c0c31f51a5ea8138e29cc003e64f90a152e271c1e104bf`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 2.0 KB (2014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `arangodb:latest` - unknown; unknown

```console
$ docker pull arangodb@sha256:719232861f5fc1613e15ab6e000e9e3413655f033221b7f319ac1f9904840364
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **680.6 KB (680593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0f3340411f9507c0cb70866ce110e0d1b209cc466417acf3c8376b2805dfa6d`

```dockerfile
```

-	Layers:
	-	`sha256:a0409960b0c1227d52bdadb01ef1da12b8943aa8a99a81e80271fcf75125d241`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 665.6 KB (665642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08f3e65214e407fdc7c0948336326a40b0a187a9f5fb2324f864e5efddf244be`  
		Last Modified: Wed, 28 Jan 2026 02:15:33 GMT  
		Size: 15.0 KB (14951 bytes)  
		MIME: application/vnd.in-toto+json
