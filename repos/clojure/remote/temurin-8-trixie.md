## `clojure:temurin-8-trixie`

```console
$ docker pull clojure@sha256:8242ecdefbc099e1583c19461cd1781eef3d124405a824bc144f870184f9997c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:40f936c6a96be80ecf8af2f505ea5106652a24c286bd12f279446091b582c74e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.0 MB (190018290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b34464601a9467e21b20f35a932c90f154ac225c1994d0ad6c1991282624aec`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Mon, 02 Mar 2026 19:46:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:46:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:46:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:46:03 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:46:03 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:46:24 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 19:46:24 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:46:24 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:866771c43bf5eb77362eeeb163c0c825e194c2806d0b697028434e3b9c02f59d`  
		Last Modified: Tue, 24 Feb 2026 18:43:22 GMT  
		Size: 49.3 MB (49293124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:155707365db6ba582fa3e1021a06e94cfc1a8caf9547219cba15eaab167c80a2`  
		Last Modified: Mon, 02 Mar 2026 19:46:47 GMT  
		Size: 55.2 MB (55170047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c9d8e93cdbb909f125bb5adfd23880b45235811ee33f4427d03a315bd782c6`  
		Last Modified: Mon, 02 Mar 2026 19:46:48 GMT  
		Size: 85.6 MB (85554472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e10a9ccf18f81d4b50ae7cda42e7e2fabb5aa8a1b9e9e8dc30e37aefd902ed96`  
		Last Modified: Mon, 02 Mar 2026 19:46:43 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:d5855c3157e7eada05b37554e3b8e2c8ae030ecfc82e68522adc941fa151abfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7605748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a3e6dd285fdb0b14a4651f5d15a46dc640abbbef2f8ef383fe83b0328204008`

```dockerfile
```

-	Layers:
	-	`sha256:69bde27ccc157f71af5cef4ac9c4da0db1faaea56038cdea41c0f6410c63d65b`  
		Last Modified: Mon, 02 Mar 2026 19:46:43 GMT  
		Size: 7.6 MB (7591580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:128548ccd44d5b362a482041915dff3935e9f4064f439408e5e2509d4c8f70c0`  
		Last Modified: Mon, 02 Mar 2026 19:46:43 GMT  
		Size: 14.2 KB (14168 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0f2e3b7bd885d95a47a313ed10fa78a8e8784355b54b9a8bc2a9a1658f7fff08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.3 MB (189282946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42f7aa8ab5b73528ed69659073af911ff36b1f529131e1b4f9372ef936eeefe1`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Mon, 02 Mar 2026 19:45:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:45:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:45:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:45:16 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:45:16 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:45:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 19:45:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:45:34 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ac9148dc57ca750b09f3f3da6f16324e1a3b62432b2726734535ec610e1a9232`  
		Last Modified: Tue, 24 Feb 2026 18:42:56 GMT  
		Size: 49.7 MB (49652168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71552ed65e5cd0155e1f2ed2f8132e3a71a6a39114f2615122f48b93f2c7d6bc`  
		Last Modified: Mon, 02 Mar 2026 19:45:53 GMT  
		Size: 54.3 MB (54251614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b63f3d45525c933579a2e7a769816284c4958376aeda244aad596fb9bc8540`  
		Last Modified: Mon, 02 Mar 2026 19:45:55 GMT  
		Size: 85.4 MB (85378516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db16f066e4ffd01826c8108c05dccd3a63fa193f1da1ff40606707106ce1a592`  
		Last Modified: Mon, 02 Mar 2026 19:45:51 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:1e75fecae8d57f3895b03bb15a427e51e7ab71a27667eae2632a96c7bbfaecf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7613598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa7df7052062b3d4c94f522afb277b47d3b8479a557f0ab954bb1d64dbef497f`

```dockerfile
```

-	Layers:
	-	`sha256:b56996615302d185ba2ae635d6f5a195c402351c2be8c7c83e05a59791ea9198`  
		Last Modified: Mon, 02 Mar 2026 19:45:51 GMT  
		Size: 7.6 MB (7599310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2647af44b54f5abb3cfb33aae8813aecb9307499f6e1de72b81f9ff645cd23e`  
		Last Modified: Mon, 02 Mar 2026 19:45:51 GMT  
		Size: 14.3 KB (14288 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:bfc46ac65d88990846fc06f77c941d42aeef39fe1c1c62311115b36571fc5518
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.7 MB (196737402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:166df6f59ac7453830e850fb3d0316a6c2a9e46128ad992b7c4e0d5b1ff5cd4b`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Mon, 02 Mar 2026 19:48:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:48:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:48:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:48:44 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:48:45 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:49:38 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 19:49:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:49:39 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:468eb7cd0e9ceb9e5b1c4c9daadd36c2fd1f1ee82c667dc1a7d70fa95600a20f`  
		Last Modified: Tue, 24 Feb 2026 18:45:11 GMT  
		Size: 53.1 MB (53112261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1cbe1d1f1f3167ddbae50f99b51d335c3b83495ac1262bf2f6c10658210c1a`  
		Last Modified: Mon, 02 Mar 2026 19:50:19 GMT  
		Size: 52.7 MB (52650396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e67d7bae47c59bb2546210b29f7eff1020397357249c0cd76cb41ec034652e1`  
		Last Modified: Mon, 02 Mar 2026 19:50:20 GMT  
		Size: 91.0 MB (90974097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b5ea82c90e63ed6baa0f36517ee5e7a03ff7f82911ddef2f742eaeba6d20e42`  
		Last Modified: Mon, 02 Mar 2026 19:50:16 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:8d58c4440842b8c3720fea0333a29a47491abb2603a001b1574408fd6455ae97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7610814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68b02e6c7ba5b532fb5955c6c199d816a2f16131dae0d83aa945e237b7c8b37e`

```dockerfile
```

-	Layers:
	-	`sha256:d94cc7060943e887f3795fc737ef04d2f850b7d38f4952b8229084997b22ebb7`  
		Last Modified: Mon, 02 Mar 2026 19:50:17 GMT  
		Size: 7.6 MB (7596596 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f3781bf04f10ea160edf92952ebacecd0d296e8b22242fbb6dd8094a27d4a0e`  
		Last Modified: Mon, 02 Mar 2026 19:50:16 GMT  
		Size: 14.2 KB (14218 bytes)  
		MIME: application/vnd.in-toto+json
