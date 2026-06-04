## `clojure:temurin-11-bullseye-slim`

```console
$ docker pull clojure@sha256:b46643027fa1b13ffeabeed1e6f66c0d77be0d47bf4e3856404d252725405483
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:f3fe1b8144a5c09b8feb53a94ed0664429898f864eda4d46e766c165ff977a76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.2 MB (232244787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8396e18a3452f3f697f3b7276abd97fba6b768e155d6d30e6f34501134c173e`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1779062400'
# Thu, 04 Jun 2026 17:44:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:44:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:44:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:44:30 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:44:30 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:44:43 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:44:43 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:44:43 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:8419f4a27c97b0c111ab0dc77e0159bd3abfadcb948d4a49cf6dd6670703b84e`  
		Last Modified: Tue, 19 May 2026 22:36:35 GMT  
		Size: 30.3 MB (30257598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9887dfd8f28edae2f5230a9054ec06a9e46dd4c2651a7b2e0679682ded046931`  
		Last Modified: Thu, 04 Jun 2026 17:45:06 GMT  
		Size: 145.9 MB (145886255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56ddf830c20fb6287b89acf78050c86bcd686cee2879760c373eb1604ec916a`  
		Last Modified: Thu, 04 Jun 2026 17:45:04 GMT  
		Size: 56.1 MB (56100288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb93b48a36f2727cdf0026acb8ed692eef332288e9655ef67f82fc56eacc0bb7`  
		Last Modified: Thu, 04 Jun 2026 17:45:01 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:43c6e117691372e68afa5da5c7decb0bdd2f60b68b81eb83e5df4bbde903fa94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5351782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb0b4c85d7451d5fdb1843a7c7736176b550339a8d541b0c7ae1360ad3c9f8b0`

```dockerfile
```

-	Layers:
	-	`sha256:e4ce1a7801d947b71000c5f944c0daa17aa6766f6f6f59ca7a1356128eb1febe`  
		Last Modified: Thu, 04 Jun 2026 17:45:01 GMT  
		Size: 5.3 MB (5337361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6630e80117be96a9df67d28dad5e44c9b763fedcb38deb5ea7f027a629befff0`  
		Last Modified: Thu, 04 Jun 2026 17:45:01 GMT  
		Size: 14.4 KB (14421 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:fd0df22566554e68228f1d181097a735e78c26540b70b0e062325cd76529e5ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.6 MB (227592901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31f57af2f2a471a1b53a3dd017e78caa01166d7f4f5df84f6aba9266ccdcaf00`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1779062400'
# Thu, 04 Jun 2026 17:44:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:44:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:44:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:44:11 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:44:11 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:44:23 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:44:23 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:44:23 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:2b99ba6638377be8e7e1e9a328ebb001513ab9f700c8168d404eed03437c7ce5`  
		Last Modified: Tue, 19 May 2026 22:36:47 GMT  
		Size: 28.7 MB (28742972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04958b1e6f95f0bf8e4d1eb768f6bb55ca75812a009961f006f16174fb559226`  
		Last Modified: Thu, 04 Jun 2026 17:44:45 GMT  
		Size: 142.6 MB (142582230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed03cad74185d989f199687ec383c2bc8f52e9d2c127aecc0e1054907d7c04f`  
		Last Modified: Thu, 04 Jun 2026 17:44:44 GMT  
		Size: 56.3 MB (56267054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef4292f0a7c82d0dd6242c34e757ef003db6357cc4771c07f57d768fb07d5a9`  
		Last Modified: Thu, 04 Jun 2026 17:44:40 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5e58a3ca5008b3c3cff8a80cb131fa1f23bac2ffbb0b3af17414059ed86d08e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5358250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdc1c94a3487dd81cd6ff6f97dc8dbebf8996df11a74be834cf6b6135a6833a9`

```dockerfile
```

-	Layers:
	-	`sha256:73deb6773c218db38caef03f398159eaa09d66852e8de646228bdd374854aaf1`  
		Last Modified: Thu, 04 Jun 2026 17:44:41 GMT  
		Size: 5.3 MB (5343711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7710c1ae81540f62d2aa9c9e47a0cc983bd2fed0c0c608d547e0c3392a7b2d1d`  
		Last Modified: Thu, 04 Jun 2026 17:44:40 GMT  
		Size: 14.5 KB (14539 bytes)  
		MIME: application/vnd.in-toto+json
