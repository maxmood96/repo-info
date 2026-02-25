## `clojure:temurin-8-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:c758c65fefa83acd1e001abcf79278af0cc58e936280b41ee9fa6fc173391309
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:d0536cda3d420cf97026c4a4b8e48a00433e9fce3b7fa3bc1b05759b2879f8c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.8 MB (184809947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87e51e8a4975faf18bfc0cb236bfd6964be7ecbd9c05deabdf7504e5580cbe6d`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:52:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:52:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:52:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:52:04 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 19:52:04 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 19:52:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 19:52:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 19:52:54 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:6a7e0620566c7dfbe5d3c9a7601d116556ec17a021b3e824f8ab09d12b0c25c6`  
		Last Modified: Tue, 24 Feb 2026 18:42:43 GMT  
		Size: 48.5 MB (48488777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e226332ea3f9c564edeb3bbde63b3c9d476d133dc336dbb442852ec2fdae2ddb`  
		Last Modified: Tue, 24 Feb 2026 19:52:33 GMT  
		Size: 55.2 MB (55170133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:275a0569b6f64e6bedb508c276ce3681c8c38021d4fa2233f9d6a876d02200c1`  
		Last Modified: Tue, 24 Feb 2026 19:53:12 GMT  
		Size: 81.2 MB (81150392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c44b07c331bd616681705cfa2a36f5c5978a1027e667fef4fb633b747d768bf1`  
		Last Modified: Tue, 24 Feb 2026 19:53:10 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:0f01aa7b61a264831d0a283e7c02a54b92ed71511207f5aa9bbf8881e081e724
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7511169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a0a9018ce976443771251af5532fe7c86e35d2c53561e285063d7d1cc659558`

```dockerfile
```

-	Layers:
	-	`sha256:d7d1a3515a92567ba0cecc7dd0a5cde9863f86bbc70514889dbc5abcc023662c`  
		Last Modified: Tue, 24 Feb 2026 19:53:10 GMT  
		Size: 7.5 MB (7497776 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d05182cfa98818233f4b0fc6efc8f8e88c9793bca71baae931b3b55580413b0c`  
		Last Modified: Tue, 24 Feb 2026 19:53:09 GMT  
		Size: 13.4 KB (13393 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4b99fcbb86387250a5480ed866484824f88a8e0f7da0fe4d0ea621432cfde156
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.8 MB (183763394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1a3943eee9074a8fbda44b6c3b70c7bd5cdab7e7e49ba89edc3e7b44b809b86`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 20:02:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 20:02:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 20:02:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:02:36 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 20:02:36 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 20:03:28 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 20:03:28 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 20:03:28 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:8578011282ae3fef36307f7e3afb2265a96bada1a57648f07bea9cc1a11e7b7b`  
		Last Modified: Tue, 24 Feb 2026 18:42:06 GMT  
		Size: 48.4 MB (48373210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5899fd4281eb802180094cd7248a180de2d7f4dd4fadc1ad27cbfc97e09414b`  
		Last Modified: Tue, 24 Feb 2026 20:03:03 GMT  
		Size: 54.3 MB (54251619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c86b412715f7bd495609651ebb01774213c75407fe03c8f99f0a85c19449b4e`  
		Last Modified: Tue, 24 Feb 2026 20:03:46 GMT  
		Size: 81.1 MB (81137919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa9fdda5e6f9f18e0bf0054750bd5cae51aaf0424b484880511f52385ab0e8b3`  
		Last Modified: Tue, 24 Feb 2026 20:03:44 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:5d2d3edb51c40ae64a50bdc9fe29a536ae4b10107f671114f5a257a01387e9fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7517749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77faffb1c0aa1262d65df22344467af2ad1cfe94d6aba67b2ab81b04b361c8a8`

```dockerfile
```

-	Layers:
	-	`sha256:9f4e21ce246a3251150dd7502b0f2ddf4b2b386a7fea76223c50fdca48955f4a`  
		Last Modified: Tue, 24 Feb 2026 20:03:45 GMT  
		Size: 7.5 MB (7504239 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d13df1ad3d2838f558b4b5d120ec607cb5eaa633d0237c1f9d688e50a2564a9`  
		Last Modified: Tue, 24 Feb 2026 20:03:44 GMT  
		Size: 13.5 KB (13510 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:3780fd8177e9cec98495bf573768469b006bb2f487dfd59df1c44ee4d0dbde85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (191974800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51fee8deb2fbb64f1068cc9b0e7042a37246aa7f305568f27a58e378b9a4cf90`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1771804800'
# Wed, 25 Feb 2026 01:40:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 25 Feb 2026 01:40:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 25 Feb 2026 01:40:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Feb 2026 01:40:50 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 25 Feb 2026 01:40:50 GMT
WORKDIR /tmp
# Wed, 25 Feb 2026 01:45:53 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 25 Feb 2026 01:45:56 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 25 Feb 2026 01:45:56 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:605d3e8e339092bb5c341e87f55fee22f143aaa738eb91d341b5fc6aa27b2b5b`  
		Last Modified: Tue, 24 Feb 2026 18:41:51 GMT  
		Size: 52.3 MB (52336797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:758957e39a5342d475126ebfd163d16c39ac530ed3ea794d3a28465b8deb3059`  
		Last Modified: Wed, 25 Feb 2026 01:42:09 GMT  
		Size: 52.7 MB (52650389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfba55139e806c41b71a9a6ac9d3f739f2ecba4aa27c97497a7b663e845a86b6`  
		Last Modified: Wed, 25 Feb 2026 01:46:37 GMT  
		Size: 87.0 MB (86986968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f5f1b27434803a6b6ff1737c2fc0f056a697c40b06934257aac591a7ffe1144`  
		Last Modified: Wed, 25 Feb 2026 01:46:35 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:c8312683d60b6002f1fac2cd032e774f573d6755f5b6cdb5aee8b50199961a9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7517829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29e243f1c871443bb9a31797fa61a4da236b8e1d7997ee1c1e8dc977ad90eda8`

```dockerfile
```

-	Layers:
	-	`sha256:4186834e9ecb804ffde23b8cccf474ef72543dbc19607e066b513e0e970223cd`  
		Last Modified: Wed, 25 Feb 2026 01:46:35 GMT  
		Size: 7.5 MB (7503587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:073d2ac107f00c4afebba415db69437fcb6aefb33ca1d324b13e500f97c9e076`  
		Last Modified: Wed, 25 Feb 2026 01:46:34 GMT  
		Size: 14.2 KB (14242 bytes)  
		MIME: application/vnd.in-toto+json
