## `clojure:temurin-11-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:ed1eb1ff7b39fb2196a5e7adea15ab1384d565cc4b8a6853462fdf9f744b4365
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

### `clojure:temurin-11-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:9eb1840eb57539e1fd0c494a030903e28d26ca89ef3c0536d44f2f31c7f3b633
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.5 MB (275462622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4600c6e7f8ab0f3616f2553db39473f57fc39a5c27c541b54194254dd8c343d7`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:17:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:17:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:17:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:17:23 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:17:23 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:17:38 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:17:38 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:17:38 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:db53381ee51f9e43304e236099ba097ae1b33ae41a8007e0b6319992eb55fd00`  
		Last Modified: Wed, 22 Apr 2026 00:15:45 GMT  
		Size: 48.5 MB (48488628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e5419099bc8f3a1a84218f3e8db04ac67fa66924d18c7afc6b3fc93293d381c`  
		Last Modified: Wed, 22 Apr 2026 02:18:00 GMT  
		Size: 145.8 MB (145806794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29b67ed0f4e5fe9fde39f76f50fc27411c4731ebe43c78641c26f4a4009c1585`  
		Last Modified: Wed, 22 Apr 2026 02:17:59 GMT  
		Size: 81.2 MB (81166554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9086095b2c3e2ca209d30bde1e0b79ae66703eb76fdaeed95f6ce45ba5786bdc`  
		Last Modified: Wed, 22 Apr 2026 02:17:56 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:333433c2b52e8fc9102fdc10369be2d380dc119b00dbd8b3daaa92a9e3373922
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7412652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5563415f3e165d31ad4591ed5985f602270ac11129892be96c8f8a09c289f8fb`

```dockerfile
```

-	Layers:
	-	`sha256:284064e9d3e25c53a4969c764c04038fcd356c52b8683ef16cc9eeb19b75990d`  
		Last Modified: Wed, 22 Apr 2026 02:17:56 GMT  
		Size: 7.4 MB (7398443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8b4b4e0c0fc485f1d46c27726c34576afedf0c0d12485747d2a37d95702c251`  
		Last Modified: Wed, 22 Apr 2026 02:17:56 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1bbbb2d59939f3fd07edf1528113d8d5978e0cc54bb480727ca17418fc062672
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.0 MB (272048641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acf6d980268377d4d69f80bfc1644f2cd5d81567e5f7a987621e399dc0298e49`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:19:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:19:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:19:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:19:58 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:19:58 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:20:55 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:20:55 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:20:55 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:30de66f8fdafab67e88d876087f571a693a1a6c4cf0abc29efbf88ea878e0d29`  
		Last Modified: Wed, 22 Apr 2026 00:15:43 GMT  
		Size: 48.4 MB (48373071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:552a5082121fb2ebd807c5a86e671730c73060a10c23300a7ce52bc5169bda32`  
		Last Modified: Wed, 22 Apr 2026 02:20:33 GMT  
		Size: 142.5 MB (142500803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8852d47d3d54241c0c6430e99ccda3a80451b36e468515152a1bbbdde6060a20`  
		Last Modified: Wed, 22 Apr 2026 02:21:13 GMT  
		Size: 81.2 MB (81174124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b833f8f1ba9eabfcb22527bf40d7f973d094a94ce504ceb2e9fec7c9f2158703`  
		Last Modified: Wed, 22 Apr 2026 02:21:10 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:bf6ee19dcfaea258e0279e0d5f124ccdf0abda567212abc654d1ffa88a0473aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7419151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31cc8b027d4d7fca936122ee98dac5d9e26832931decf0a26449e7cf997a8bf9`

```dockerfile
```

-	Layers:
	-	`sha256:1d7bcd8fdfde7a166dbf7f246d5bf06142bed15f8deaceee5ca42c80783e6a0f`  
		Last Modified: Wed, 22 Apr 2026 02:21:11 GMT  
		Size: 7.4 MB (7404824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae342d99448533143ed8a244f52f3e5442a3fea3bd451f0bcb0bf077238d5ba6`  
		Last Modified: Wed, 22 Apr 2026 02:21:10 GMT  
		Size: 14.3 KB (14327 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:fc9cc3c93fc3d916b90712599d8eb86267eed8e58857f26ab1caf7ba4e3bdd1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.3 MB (272339270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8571652b3164b5b86074a87b1d9d2096d8708717f0acc16811299e9ad3a7cb48`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 08:20:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 08:20:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 08:20:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 08:20:35 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 08:20:35 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 08:25:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 08:25:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 08:25:22 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:0b84f035435acf0ec33df4748d96fad1243fd6b0ea9917f29eaa507d4c458365`  
		Last Modified: Wed, 22 Apr 2026 00:15:04 GMT  
		Size: 52.3 MB (52336735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a601f15c2ddb40a58c5c2980085dbdd555e6ed8d434c0c8e7d30d094422dd20e`  
		Last Modified: Wed, 22 Apr 2026 08:21:58 GMT  
		Size: 133.0 MB (132997391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e782b91f35bf7ec3d941b66ecd0615dbfd2ee68b9e0739403ee7e0a4ff138dd`  
		Last Modified: Wed, 22 Apr 2026 08:26:04 GMT  
		Size: 87.0 MB (87004499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b64eea35274c55cd6ba8b9ec6ded5744aa1061f04e3abbcec17a3d83cbd12604`  
		Last Modified: Wed, 22 Apr 2026 08:25:59 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:bf83b318a1f21509e4b13f58e5e3d0c6680fefa1fdd085aa466355963eb77275
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7417301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ee0ded11fbbf3217947f9972844a7ee9727d19a7bf8425ff2b988a59e833dfc`

```dockerfile
```

-	Layers:
	-	`sha256:c4601e7601792c5a0bf82debd0b5a22f861e8f7d10c3d559f80cb1f75f6606d4`  
		Last Modified: Wed, 22 Apr 2026 08:26:02 GMT  
		Size: 7.4 MB (7403044 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:939dccf4873fe382717af408312341bcd98f50bdb71efdac4971cafa864c4755`  
		Last Modified: Wed, 22 Apr 2026 08:26:01 GMT  
		Size: 14.3 KB (14257 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:f07ab984199d4439b7afe29e594c3b7227b376c7c0e4f85995a2f46625def66b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.7 MB (253690536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b6bedfdb2929721241dc1c8e832dc4b4fd11b117226c42e14d7ee0facf6535e`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 03:58:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 03:58:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 03:58:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 03:58:25 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 03:58:25 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 03:59:38 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 03:59:38 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 03:59:38 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:65a8acd2327b0f3316fe8707ebd5c99b15e79306d4eca71f3e635588795ae2bb`  
		Last Modified: Wed, 22 Apr 2026 00:15:31 GMT  
		Size: 47.1 MB (47147970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e8e0b2edc82a3ba082e9f30dfa4358139881cfd62d2d6d055012699a091c83c`  
		Last Modified: Wed, 22 Apr 2026 03:59:03 GMT  
		Size: 126.6 MB (126562180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:091a03b7d18cfbc1193c2b55ff8e661be25f67fef39d5490f9b6aacf742a755d`  
		Last Modified: Wed, 22 Apr 2026 04:00:08 GMT  
		Size: 80.0 MB (79979741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd42e17401e27ddb87c7375a6b40e2aa492c36040031ece9014941b82972b3c`  
		Last Modified: Wed, 22 Apr 2026 04:00:10 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:be3af0284db2dbe76b4c9d887b4aa1211d0d4a84b56b5ad6595396433dddcd4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7403975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fce866bf4044b52e9e99b72a12f60b39bbc265023cf1ae74154d860ef23483f6`

```dockerfile
```

-	Layers:
	-	`sha256:94529d99d826a93bdb4b82b75e98f0f231acbc4aaad4b9018db37a418b4e3fce`  
		Last Modified: Wed, 22 Apr 2026 04:00:04 GMT  
		Size: 7.4 MB (7389766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e6ab35e9889c625f5bf6b3ca294ee1f825a0f50ab8b3b58f7e74aa34a669a1c`  
		Last Modified: Wed, 22 Apr 2026 04:00:04 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json
