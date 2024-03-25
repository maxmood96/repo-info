## `arangodb:latest`

```console
$ docker pull arangodb@sha256:d7b59ffd036db30e8813be71a4d0e0d930af1ab59480cb8f7666fc9e56d5bf05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `arangodb:latest` - linux; amd64

```console
$ docker pull arangodb@sha256:7f1fbd60dbf77a4085cfba8c202ea83b523e474c8c22fe6f8f5c76ad3d684ea5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.2 MB (208229724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b60587c2ed005597247dfe74d015d162580bfcdd49cec5824117e8b740543573`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
CMD ["/bin/sh"]
# Mon, 25 Mar 2024 19:51:03 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Mon, 25 Mar 2024 19:51:04 GMT
ENV ARANGO_VERSION=3.12.0
# Mon, 25 Mar 2024 19:51:21 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Mon, 25 Mar 2024 19:51:22 GMT
ENV GLIBCXX_FORCE_NEW=1
# Mon, 25 Mar 2024 19:51:22 GMT
RUN echo "UTC" > /etc/timezone
# Mon, 25 Mar 2024 19:51:22 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Mon, 25 Mar 2024 19:51:22 GMT
COPY file:513375723ea161120e77fe867a15962ee909f21d5ad9010e94f567e75f817d04 in /entrypoint.sh 
# Mon, 25 Mar 2024 19:51:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 25 Mar 2024 19:51:23 GMT
EXPOSE 8529
# Mon, 25 Mar 2024 19:51:23 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ecdd28207d9bd85310dbf913e40d273fb64797a3f1333cdd213571aeff650f8`  
		Last Modified: Mon, 25 Mar 2024 19:51:55 GMT  
		Size: 204.8 MB (204848166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1841e2292362b1cf6a93ff6be80899cd59863261282ee8867197f46705a60f6`  
		Last Modified: Mon, 25 Mar 2024 19:51:37 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ae8881e8aa2f1c444ade1abd168e516802ca7ffdab5ddf0e2007d384555cdd`  
		Last Modified: Mon, 25 Mar 2024 19:51:37 GMT  
		Size: 2.0 KB (2015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `arangodb:latest` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:209ddde51cbb4ccf144c4fd53ebb8fd449e2713e67c317f76cf7de8d6033a418
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.0 MB (210020640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3eb15430a24d9e671b819d9c79586ad8827f98e4e041269faaa21c7c05b6308`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Fri, 26 Jan 2024 23:45:00 GMT
ADD file:c3b6b575eb741f914ec12bd4df43de0cb044a1f2bae7ff15d176e49b5986d903 in / 
# Fri, 26 Jan 2024 23:45:00 GMT
CMD ["/bin/sh"]
# Mon, 25 Mar 2024 20:07:26 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Mon, 25 Mar 2024 20:07:26 GMT
ENV ARANGO_VERSION=3.12.0
# Mon, 25 Mar 2024 20:07:46 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8003EDF6F05459984878D4A6C04AD0FD86FEC04D &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb312/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Mon, 25 Mar 2024 20:07:48 GMT
ENV GLIBCXX_FORCE_NEW=1
# Mon, 25 Mar 2024 20:07:49 GMT
RUN echo "UTC" > /etc/timezone
# Mon, 25 Mar 2024 20:07:49 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Mon, 25 Mar 2024 20:07:49 GMT
COPY file:513375723ea161120e77fe867a15962ee909f21d5ad9010e94f567e75f817d04 in /entrypoint.sh 
# Mon, 25 Mar 2024 20:07:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 25 Mar 2024 20:07:49 GMT
EXPOSE 8529
# Mon, 25 Mar 2024 20:07:49 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:5385a9a590c3e2872b3ed27554a56fb7ce544c694b41b9b95d70fa86f30b0566`  
		Last Modified: Fri, 26 Jan 2024 23:45:40 GMT  
		Size: 3.3 MB (3258283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11fb6132dc2c94d5d221a090bee94fd9e2c67ad29d3253112aa3189d14c0e7ff`  
		Last Modified: Mon, 25 Mar 2024 20:08:19 GMT  
		Size: 206.8 MB (206760203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7205ef234cbfa94927d997e215cf7f9eb1f7df6965cad485533e224133421650`  
		Last Modified: Mon, 25 Mar 2024 20:08:05 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8db282981a6d0c329fe786daca4f84bfd2455c13d5887453ed53e0de0e5a598d`  
		Last Modified: Mon, 25 Mar 2024 20:08:05 GMT  
		Size: 2.0 KB (2015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
