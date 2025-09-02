## `clojure:temurin-11-bookworm`

```console
$ docker pull clojure@sha256:7114bac8052ae6ff0ddf2ea6ce5a71215c11c8a2d0b036861b6931bbfdecaba5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-11-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:de039c0dd3a4842d2f5e0499c7562c9cdb988efe5c348b888157cd55f37f3a07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.3 MB (275291495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b5a76764ff237b16a1f1ed5a6cf3c63214322675c8f55eb3642f70b07e31db3`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:f014853ae2033c0e173500a9c5027c3ecffe2ffacbd09b789ac2f2dc63ddaa63`  
		Last Modified: Tue, 12 Aug 2025 20:44:32 GMT  
		Size: 48.5 MB (48494511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9948923c6c177074ecf786ce1c9254647c8324cb424026e2d81786ee2c74b88`  
		Last Modified: Tue, 02 Sep 2025 00:17:19 GMT  
		Size: 145.7 MB (145658229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6e145ba066b0a17c09c903bab1bb4f97bbcbffd6d08fdcaf024a0645f3b15b9`  
		Last Modified: Tue, 02 Sep 2025 00:18:03 GMT  
		Size: 81.1 MB (81138108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b74d8b047bbf24377f67fc3e8756c88c1d698e78407ec97d016c54b00bc8f1`  
		Last Modified: Tue, 02 Sep 2025 00:17:53 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:cf80a3f635be9466b950df0af6176503ceb34a1e2d1699ebdaa5f8b2345fefad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7402690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:722309a3c6331a1a2beba37646425019be0a9b810abb5ac4b8fc03325971459f`

```dockerfile
```

-	Layers:
	-	`sha256:16a49543f1c3c0a08a6bd03ce4802091e16f01e3f4091bd2e00a8dd5be3d6426`  
		Last Modified: Tue, 02 Sep 2025 03:35:23 GMT  
		Size: 7.4 MB (7388438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe7f78517de6b21a1fbe595148a9d3c1286a72ac50e1dbdcad6faafbc9e5df43`  
		Last Modified: Tue, 02 Sep 2025 03:35:24 GMT  
		Size: 14.3 KB (14252 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d24708ba48899b9558fc9b547c69c015cbef594f94ea2e5a0b81149fb554cfce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.8 MB (271813042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c593314058e846d4d7a641920243c3e1fd0ec01affecae11f20af08e6ec08fcb`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:35f134665ae4469a16b5b7b841e9efe6b186960e0533131b3603e4816aabeb3a`  
		Last Modified: Tue, 12 Aug 2025 22:08:09 GMT  
		Size: 48.3 MB (48342450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e17e393506147fbd7055e29d89728a0fc86ede72088d0c45d92332a69b6e1676`  
		Last Modified: Tue, 19 Aug 2025 04:20:50 GMT  
		Size: 142.5 MB (142460572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ddec2d8475df0bda3c4e076dbdad69eba91387c4533e12f2edba7c633a13ca1`  
		Last Modified: Tue, 26 Aug 2025 17:35:26 GMT  
		Size: 81.0 MB (81009373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3443ee9d7fea7e39c5fb095e7ff980efa5e33db9a36d108c37b9b551e801a4`  
		Last Modified: Tue, 26 Aug 2025 17:35:07 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:267142f0b55d5dea989220a64d589a7f34e97a0e86d75c446c33d6534b0e4ae8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7409189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0423ee511af4fde177337c75871a21620193e67fadf23549603a18895b27ad9`

```dockerfile
```

-	Layers:
	-	`sha256:f539f705ddf3f374003d7f0b3693adfba62521762d286657dd6d6b4ae55d23df`  
		Last Modified: Tue, 26 Aug 2025 18:35:11 GMT  
		Size: 7.4 MB (7394819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb903832da9c0db05bc03a28bb20e9c111bfb4eb3989328338e69ec253064088`  
		Last Modified: Tue, 26 Aug 2025 18:35:12 GMT  
		Size: 14.4 KB (14370 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:102aff611e3d1d97d7694083f94aa21de4bbfa9416476957e6dab83dcec4d33e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.2 MB (272164585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69e9551b5fee88b093f4d6e9fb4b85a1861319752a3cf91f24f9fea4d6e8f6fd`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:33bc01697f2fcceb00fe53fe1bf433b48dc127c82c1555f61eeddeda9d72ff40`  
		Last Modified: Tue, 12 Aug 2025 23:05:53 GMT  
		Size: 52.3 MB (52338077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c0cbc261facd2ea551ba4f1d307ad561b88de934025d4d92da0a46a7a5d5385`  
		Last Modified: Sun, 24 Aug 2025 07:13:30 GMT  
		Size: 132.9 MB (132853318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:993bdb2865ec883ece8a2f28d83d97bc8ea76ca5a6f4358e1e144f6130721bfc`  
		Last Modified: Tue, 26 Aug 2025 23:08:56 GMT  
		Size: 87.0 MB (86972544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dee3c5b71fbb62ac1e64316a2848335d1383a0d151ab5ff6b31a53b04b8a72fe`  
		Last Modified: Tue, 26 Aug 2025 17:45:42 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:93496c7cd70388de4a822f73e55c8439c539e7f308c2675fb928bb9077e8c158
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7407327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9ca8a374b0cbf5613c11ad66a211326b8d1e4ec5c93bcc5bb3a6c4da03f4658`

```dockerfile
```

-	Layers:
	-	`sha256:ae3b992f4e92427d032a4770def843d6933c28a9367f774c94723d123796411a`  
		Last Modified: Tue, 26 Aug 2025 18:35:20 GMT  
		Size: 7.4 MB (7393027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:000360117a8cb6d6e61410db46fb52c6ceae4006cdd8f7d8f2b6425686e92e77`  
		Last Modified: Tue, 26 Aug 2025 18:35:21 GMT  
		Size: 14.3 KB (14300 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:0d46837cd8cd60a4f06e73d3e04bab50d5ede0ed6b013fcfa91cd2415c760499
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.7 MB (252726543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4eba8ca3b984597caf5efec1bff46fd4103ebf140a5e1188a5ed4764fda06d3`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:635b31fd21bf059b6af0abf57b343066d0218ebb3e0b679927cc1752427a72da`  
		Last Modified: Tue, 12 Aug 2025 20:53:37 GMT  
		Size: 47.1 MB (47149866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d47acbec51e8b49420ca54277b6b3c563cc58e460f494d612b9455da60c70c3`  
		Last Modified: Tue, 02 Sep 2025 01:44:23 GMT  
		Size: 125.6 MB (125622202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0591d9f09d1ef5cf907a1e9c396641d9771e33cc9b052362fd70bb45b8e4a80e`  
		Last Modified: Tue, 02 Sep 2025 01:51:03 GMT  
		Size: 80.0 MB (79953828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f538cdf57e5fb30be540352c6902e5711da3a248ef7ab548eb64cc352521f0d`  
		Last Modified: Tue, 02 Sep 2025 01:50:46 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:18a9306121f4b42e818ae6f9fde8921dcf19ac3780e5da34f76c283cecae3982
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7394013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aee7a942e7d56c8c72aa3054ccdd4f34ceab367ffc8e7f85994bb839f8f23cf`

```dockerfile
```

-	Layers:
	-	`sha256:8259d20479a544d30be70276b8be0d199f6b7b526f0c81cdb029cca2cc04dcc7`  
		Last Modified: Tue, 02 Sep 2025 03:35:42 GMT  
		Size: 7.4 MB (7379761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6836bc2c33385de653f5fb6b186e7034a312c88d06450700e61d04234e39cf16`  
		Last Modified: Tue, 02 Sep 2025 03:35:43 GMT  
		Size: 14.3 KB (14252 bytes)  
		MIME: application/vnd.in-toto+json
