## `clojure:temurin-11-bullseye`

```console
$ docker pull clojure@sha256:3f2a1b4014ff51abf60dcd083137cac36f99c86c22e566c3462032e13470137b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:789f6e505b8dc816fc599f17a03f344339dc8e6fab3702825f55fcb9e82dfd52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.8 MB (268780524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58528ee5d1277bf371895d6f06d427b044833d468d7d7c6e090e254221b0638b`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:23eb0befa94abc6ca44ad0270547b7bc53b5bcca6a4d44d4f9fa2a658cdbaff5`  
		Last Modified: Tue, 08 Apr 2025 00:23:40 GMT  
		Size: 53.7 MB (53748529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50bdacd2bba554949e85c451e3ea78d20039b927e50efb984d6610f0f19b742e`  
		Last Modified: Wed, 23 Apr 2025 17:15:43 GMT  
		Size: 145.6 MB (145635867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:663426e8707340f0f8f132e88925c365dde5a5ae6e2646b288d0214e31aadcd6`  
		Last Modified: Wed, 23 Apr 2025 17:15:41 GMT  
		Size: 69.4 MB (69395481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da9660fb207d07da7f2453cbb4a395a32c49f2130841fbc057447f77b219b788`  
		Last Modified: Wed, 23 Apr 2025 17:15:40 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:88ac8d0b5e402b2788097de8d390cb9c9237d8b735dcd59c87eecabf6ae4409a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7240894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f539032d884da02d434c5350b89602a47192962208d98b3ef4395d77150ae18`

```dockerfile
```

-	Layers:
	-	`sha256:bbd98c3a27f35a6a1502b09c53a0961666564356e7f34e1b99b6add2454b7481`  
		Last Modified: Wed, 23 Apr 2025 17:15:40 GMT  
		Size: 7.2 MB (7226642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2c0d37b5f59cdacaf411155271c422f9097a6cb37ec0fbbedcce082e12ded44`  
		Last Modified: Wed, 23 Apr 2025 17:15:40 GMT  
		Size: 14.3 KB (14252 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1a2ad3ce6e180aac6a93bb57e7a9c23a0c9ebaea36716cda4ce24fe4d59f619a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.2 MB (264206154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:051759ab1397979c2568181d893fb03b03697a73cd19578f215829d1c928f788`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:75f90a7fcbe0fba15646899ff45dbbdeecc9661d3b9445f4ef346d30119fe345`  
		Last Modified: Tue, 08 Apr 2025 00:23:22 GMT  
		Size: 52.3 MB (52254222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6547976fd91789f51bff85ffd649e7a0f8f7fc9fdd76aef7c938698e4a3ae156`  
		Last Modified: Wed, 23 Apr 2025 19:37:50 GMT  
		Size: 142.4 MB (142422063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b61f3f0a012780c00bc2e9b4a37c89aca2ef54d4b9d68eec4bcda0d33455012c`  
		Last Modified: Wed, 23 Apr 2025 19:42:31 GMT  
		Size: 69.5 MB (69529222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad41899cae85ad5843092b603d0c689ca908ee72964d163551fcc15bdc6c07fd`  
		Last Modified: Wed, 23 Apr 2025 19:42:29 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:56802199480bcdd444c1949e0b3a878ce65ff95189e86f3a1a38dc7a7015b7d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7246729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beb008b5a313dbbcbdd24361533ed25b39cab1366343ec596a323d91c7facf79`

```dockerfile
```

-	Layers:
	-	`sha256:a93dcc2362bc038311bb236a65a1433748eef2b123256bcf1c0d30fd413d4726`  
		Last Modified: Wed, 23 Apr 2025 19:42:29 GMT  
		Size: 7.2 MB (7232359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:336f0b02f51dfeef8c66580a31e70d5910f8ecef2df2067c452c040da27ac682`  
		Last Modified: Wed, 23 Apr 2025 19:42:29 GMT  
		Size: 14.4 KB (14370 bytes)  
		MIME: application/vnd.in-toto+json
