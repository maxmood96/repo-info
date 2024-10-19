## `clojure:temurin-8-bookworm-slim`

```console
$ docker pull clojure@sha256:83052626bd9dc2d65693b3cb1fe5ddbc9fad6e076770ae4a83e37ec04e864397
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:dc7d5c13a49b199f3d39cc1277520db2f299e60d04db108bea917ea75f4ae52e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.2 MB (202221585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf9acd9d72a278115cf97df359a601f81aa1d5e8b6446afbb9b18e21e2122828`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ed0be48c44c66a5e07342d99a681695f792578469dd88ed1512ce875ecde84`  
		Last Modified: Sat, 19 Oct 2024 02:55:12 GMT  
		Size: 103.6 MB (103611910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7a30d4f8bf8100e3a743db06481d5bf4f621640fae74e4296b4be002a227dd`  
		Last Modified: Sat, 19 Oct 2024 02:55:11 GMT  
		Size: 69.5 MB (69482741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eb864cab0b97cecf8d4adcce85788081dbc55045e9e99fd8492f9ef83187c22`  
		Last Modified: Sat, 19 Oct 2024 02:55:10 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:367c2823c486d1cee56ed5a4862aeab1c865653258ab438d43fd94fb80d8624f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5056892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68d60ad112256727b181b49412e738076e069bdc124e4e8d417393965e232647`

```dockerfile
```

-	Layers:
	-	`sha256:6b2e71939e88d6ea6179c4ac0a8a8dfb1f1dbe1c2722e212ffeefd2ad95376d3`  
		Last Modified: Sat, 19 Oct 2024 02:55:10 GMT  
		Size: 5.0 MB (5042762 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a775c53d1c8365963d66c8aa2d7a0019633b88152b1d94c7ef9c3ff3c859292b`  
		Last Modified: Sat, 19 Oct 2024 02:55:10 GMT  
		Size: 14.1 KB (14130 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ea6ac39d21aed385cf06895d149d827f06836a32c2491781fe5025efe507bae3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.2 MB (201231454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf858d1771a32e7f33499b30f283bf8e63ab74c8433e1ef491295aea6bdeb623`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df4d3ab9f9f5e11b08623fe806247e07bf17740018797c1594cc65ba4f34f7b2`  
		Last Modified: Thu, 17 Oct 2024 07:56:41 GMT  
		Size: 102.7 MB (102729259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa5ec7254addbc4961aa50bc992a3a5817b8aaaa3125022646062ae6e21ee06b`  
		Last Modified: Thu, 17 Oct 2024 08:00:35 GMT  
		Size: 69.3 MB (69345210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a3ca03a6c0b0e8d1bcedbc0b77ea6466883bfb5e737eef86ab1713524bd984`  
		Last Modified: Thu, 17 Oct 2024 08:00:33 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ed99dce5df287dd738cf74ff5d8d91e5721582648c08f9b1033476b66e66c0d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5063469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81bd7df662f94af2477a2abbd8f89a42c185d54a1f6e0dfb8d057473271e9c71`

```dockerfile
```

-	Layers:
	-	`sha256:4cd5279f882f86080c13638401ed99c06d3506767811b08c345c3df695abb528`  
		Last Modified: Sat, 19 Oct 2024 11:44:40 GMT  
		Size: 5.0 MB (5049227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a38ad869755940cd60f21fea5271177fead21db456e86a7a5f1c29e60b1bcb9`  
		Last Modified: Sat, 19 Oct 2024 11:44:40 GMT  
		Size: 14.2 KB (14242 bytes)  
		MIME: application/vnd.in-toto+json
