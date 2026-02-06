## `clojure:temurin-11-bullseye`

```console
$ docker pull clojure@sha256:499672f748970c41f100c81322b0c01a387426f4a9f774fe12b33ea5660fd8c4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:a9825b3d46320dc8e1f7b9e007016b3c7594543e6548a8c2f136aac0e9c837c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.1 MB (269105500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a939ce7b42a5eb8f914a5de07f6a434e0bb9b0f34424f152a9bf28fba2d5519b`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Thu, 05 Feb 2026 23:02:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:02:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:02:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:02:51 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 23:02:51 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:03:06 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Feb 2026 23:03:06 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Feb 2026 23:03:06 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:4837b8a287e31893a57c67e4e7e49ea3681edb8424480549d8b5f5b29691313e`  
		Last Modified: Tue, 03 Feb 2026 01:13:50 GMT  
		Size: 53.8 MB (53756259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:778d1eac6c1047c776d6cf568c56a0b7a2e7ce3fd803ad7d61952476d77b2b8e`  
		Last Modified: Thu, 05 Feb 2026 23:03:29 GMT  
		Size: 145.8 MB (145806888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63c40114d4c59e516e2c78440c20371607713b57a7c06c745f2481e0d8a0cd15`  
		Last Modified: Thu, 05 Feb 2026 23:03:28 GMT  
		Size: 69.5 MB (69541706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf595898c0b73cd715fec1fe9d649332d3ea51e59dc66a766be03c14193c0b0d`  
		Last Modified: Thu, 05 Feb 2026 23:03:25 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:02f2499a0344c63d5010216be3d13529746e5233a6ab265446a90e6cd5b0c772
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7432070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0259a2cbe5bc0728a37d95594b543b7232c6902cddd32daad16ec6ce10cb29d5`

```dockerfile
```

-	Layers:
	-	`sha256:d40c727c1178aa5902593776e1cae31367c896619da369d2b0bac45abb4a46c2`  
		Last Modified: Thu, 05 Feb 2026 23:03:25 GMT  
		Size: 7.4 MB (7417861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13b02de2bb67b617e59e97cdfd045937663f46844445a5abf5772f4a16daa841`  
		Last Modified: Thu, 05 Feb 2026 23:03:24 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:fe6d4d215e24791b44b06898a3f95a88894c50511de10c5dabcfafa5ba4a7cc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.5 MB (264453218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0bcc245eb0f0a16c82b3036edf0c2aac47a499c9e607d8bbea3d50829faca36`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1769990400'
# Thu, 05 Feb 2026 23:04:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:04:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:04:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:04:07 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 23:04:07 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:04:21 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Feb 2026 23:04:21 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Feb 2026 23:04:21 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:0742c20cdb1eb0c212cefb0ff441553e29e6ccfa92b808cca3d7e8548a6fd569`  
		Last Modified: Tue, 03 Feb 2026 01:13:54 GMT  
		Size: 52.3 MB (52258320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ae907bb127f6524d1eafd7657f16ba8616c2f7f3acb3aa5c71d8f6746490ecd`  
		Last Modified: Thu, 05 Feb 2026 23:04:43 GMT  
		Size: 142.5 MB (142500854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:611e7a2b115aed12dc568845f343b9241d65c983f6a7041db386c114d62f88ea`  
		Last Modified: Thu, 05 Feb 2026 23:04:42 GMT  
		Size: 69.7 MB (69693397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0707b4ab7fb78e4b6537f8796433f8a0eae97ffa5ac97714f357d1f0abbe0f8`  
		Last Modified: Thu, 05 Feb 2026 23:04:39 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:0cc4e1083f816f636a30fdfe48b22cf54471784c31348e0588de786d801204ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7437905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecc9bf7163de3393b9bde0aa85ae18c31f27c0ad711e0d3ad0eccd87669bef71`

```dockerfile
```

-	Layers:
	-	`sha256:a9e8fcdc83ffe09e73b1b1d624f0d5a667b9bd289664384d6df545b793eb7a05`  
		Last Modified: Thu, 05 Feb 2026 23:04:39 GMT  
		Size: 7.4 MB (7423578 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71faef5bc14a49df2584c0bd548e2e13b33a9a14f23c3b06c578aefcafa3ed74`  
		Last Modified: Thu, 05 Feb 2026 23:04:38 GMT  
		Size: 14.3 KB (14327 bytes)  
		MIME: application/vnd.in-toto+json
