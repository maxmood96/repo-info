## `clojure:temurin-11-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:87299a1e346008e1912bab697a27132dc357f25d29bb30934e9bf18c987013df
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:0ed110b22b98cefe66378d5cb9c61a492ef12777dc834a5971ad41fe209b7ab8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.3 MB (269257651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bf3c934809bbba1c73839bc06da14654db9a2bcb0ef14783d0cf713e9c96030`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1779062400'
# Tue, 19 May 2026 23:57:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 May 2026 23:57:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 19 May 2026 23:57:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:57:58 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Tue, 19 May 2026 23:57:58 GMT
WORKDIR /tmp
# Tue, 19 May 2026 23:58:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 19 May 2026 23:58:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 19 May 2026 23:58:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:d0d98eecfa3b5c942eada879fdb4cf6f79f0b9612ede79322d9d16fc3e984ee0`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 53.8 MB (53768852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:879dfa475d6a0bdb7f450bdf2bd204311ed57f89127b485e6b09769fa025f0ac`  
		Last Modified: Tue, 19 May 2026 23:58:35 GMT  
		Size: 145.9 MB (145886244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3092c31ad408faae50ff279cf9677bfd5dad69e9eaa83af370de5e2fe57776`  
		Last Modified: Tue, 19 May 2026 23:58:33 GMT  
		Size: 69.6 MB (69601910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bfc89c7e6a4ea7f5f123a9cd0ecd9fda693dc2e9452e6939a5a95ca8e3123f2`  
		Last Modified: Tue, 19 May 2026 23:58:30 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:9edb90e1aaec221fbf3af12d04fa96c81e8606af3e64bf5e13b00fd5fd5446b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7442157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a62f448bce571d85f81ef8d5ed418f0ad74af6efb957abe423035443b648ca7e`

```dockerfile
```

-	Layers:
	-	`sha256:13bd31292943526e0642e7f610bfb933392b47670b742da48d84815abb31b490`  
		Last Modified: Tue, 19 May 2026 23:58:30 GMT  
		Size: 7.4 MB (7427794 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b254681388379a3796a26f71f3af4435c2b99b58bd2dc12f33b48b01e0663034`  
		Last Modified: Tue, 19 May 2026 23:58:30 GMT  
		Size: 14.4 KB (14363 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d7856aea36fea8ca7db597ee8432df402f1956a2d62be6e9ae13e912e65b04e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.6 MB (264610406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f75c0dc1b82b462ba32b324888c49f022139b4d60936fd81ccfb8c94bca4c33`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1779062400'
# Wed, 20 May 2026 00:04:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:04:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:04:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:04:59 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 00:04:59 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:05:13 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 00:05:13 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 00:05:13 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:9f08527663b6ddbac974253d3632db7fd8c400d9acb6601fc251de137ec53a8e`  
		Last Modified: Tue, 19 May 2026 22:36:30 GMT  
		Size: 52.3 MB (52256578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bbfd30cb2a8cbfee14434681325c78ecdad94fef5e41948b112f53df08edc0b`  
		Last Modified: Wed, 20 May 2026 00:05:35 GMT  
		Size: 142.6 MB (142582228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dff9a3ac4f4d0051e53a5381282a5e53ea260456ce8d9eb3f8816e2ca1272a07`  
		Last Modified: Wed, 20 May 2026 00:05:34 GMT  
		Size: 69.8 MB (69770956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb2729f042edb9f0abf80f4cd56500dac87bf5c9eeeb47d43a77f201d150a5b`  
		Last Modified: Wed, 20 May 2026 00:05:31 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:7cf25165250f62d49a6e77222bbefedf72d3940bc4e14700b01fe20aad43c24b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7447992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c269da17b07de959680b79f0cf8d869ca7fbd7dbf01e096dd45d7aa9f691639`

```dockerfile
```

-	Layers:
	-	`sha256:a0f7118c12a29ad85d8c9ee26d1a3d68aa0228fe2e01f5794e15ba054d728c09`  
		Last Modified: Wed, 20 May 2026 00:05:31 GMT  
		Size: 7.4 MB (7433511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af9e2d5bedb0c85d8167b221799a14681883e9cffe9877ecd84b7ab4a2f4d550`  
		Last Modified: Wed, 20 May 2026 00:05:31 GMT  
		Size: 14.5 KB (14481 bytes)  
		MIME: application/vnd.in-toto+json
