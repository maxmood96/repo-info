## `clojure:tools-deps-1.12.4.1602`

```console
$ docker pull clojure@sha256:e055dd73b0f44b92b198eb4a2f27f534938ca68c687153af967b391b71184585
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

### `clojure:tools-deps-1.12.4.1602` - linux; amd64

```console
$ docker pull clojure@sha256:968e0d927b6f634ae81bb63ee966aa3d38787aa28f4009cd928f7c7431c3384f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.7 MB (221678316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e1ca941096ff59ecacf7b715455469ebf0fc6128f817c4c183d21a28cf19489`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Wed, 28 Jan 2026 18:06:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:06:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:06:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:06:22 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:06:22 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:06:37 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:06:37 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:06:38 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 28 Jan 2026 18:06:38 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 28 Jan 2026 18:06:38 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c1be109a62df95316ceac87ea501079f32e17f36b636865a860841b7db06100c`  
		Last Modified: Tue, 13 Jan 2026 00:41:15 GMT  
		Size: 48.5 MB (48481622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b3b8b7cd05f79824bfbe4c261f1b7434af80b9d16c1641e32c936df353e1225`  
		Last Modified: Wed, 28 Jan 2026 18:07:01 GMT  
		Size: 92.0 MB (92045314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02fdcb7bf8c7de2b98aeaed44420c0c66592f94df329ff6e09e2b2fb5e4eb84c`  
		Last Modified: Wed, 28 Jan 2026 18:07:00 GMT  
		Size: 81.2 MB (81150340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f89ca1a7e11f5074b0584376cfcd685bae989d0f96b8ef449d1b58a6f6430d`  
		Last Modified: Wed, 28 Jan 2026 18:06:56 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d93f034a0c7ce79dbb7f979b34fe09c65fecb29f5cee6873378f0e7e7b8f2e74`  
		Last Modified: Wed, 28 Jan 2026 18:06:56 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1602` - unknown; unknown

```console
$ docker pull clojure@sha256:0d3331000e384ed845fd32d2e26452ec7ef8a7120f46d8d9e0bd9fe335c83db1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7345970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4719dcecddcbba2b3a400ba42fb2f19918c0a4db8a458779c45617b21c2ce20a`

```dockerfile
```

-	Layers:
	-	`sha256:4639f717518afc6cb00f393e3736c2b181f174b4236d4054ca89b4ee0792546e`  
		Last Modified: Wed, 28 Jan 2026 18:06:57 GMT  
		Size: 7.3 MB (7328199 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d970e1389804d6da295086ebeeca4c78e588baefc5cdc60fb5ab200202af153`  
		Last Modified: Wed, 28 Jan 2026 18:06:56 GMT  
		Size: 17.8 KB (17771 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.4.1602` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e287261e1979d673d00b1033378df329c9bdadfb672a3bb0870ed2bbee959b96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.6 MB (220557859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2063e6056b065526c787f7d3380695887e74830dddad92090803dd82f899e79`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Wed, 28 Jan 2026 18:06:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:06:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:06:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:06:21 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:06:21 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:06:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:06:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:06:37 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 28 Jan 2026 18:06:37 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 28 Jan 2026 18:06:37 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1029f5ddc0d24726f1cefbb8def7a88f8ec819a1fdc4c05ce523011b4b73c72d`  
		Last Modified: Tue, 13 Jan 2026 00:41:14 GMT  
		Size: 48.4 MB (48366072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5addb7ce8e8a5a37c93a1305c42dc1d53bd2fb0900ec7c2ee03d1919b99309c`  
		Last Modified: Wed, 28 Jan 2026 18:06:59 GMT  
		Size: 91.1 MB (91052476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b02d3409f42e85a6d40e58929ddf641b1a85fcea1e29c44aa45af1bec86b430b`  
		Last Modified: Wed, 28 Jan 2026 18:06:59 GMT  
		Size: 81.1 MB (81138271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0ae471303774a93dcd9ea339a970ef50c1623d6256c99891394c1ba0b8dc19`  
		Last Modified: Wed, 28 Jan 2026 18:06:55 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dddd4d1bede5c5fc709678d62618f221aacbea73e298be4be375866e981cff4a`  
		Last Modified: Wed, 28 Jan 2026 18:06:55 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1602` - unknown; unknown

```console
$ docker pull clojure@sha256:f8b8741ab999c57e40224f90fbe0bf80b5ef1880cbba71d51f0701a4f763eea5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7351992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c9ddaf9a4f3b19409a049146aecd4636c71412e907f94707123ff1348ce431d`

```dockerfile
```

-	Layers:
	-	`sha256:497bcfb448c117251e4bd17c94f4243c88c3abec39bac2f5878d8d833d7f1e9e`  
		Last Modified: Wed, 28 Jan 2026 18:06:56 GMT  
		Size: 7.3 MB (7334031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d831e64b5dc76f5b0a46a7d632229255b72d768c743ffe35f982c1f76cd2dc9a`  
		Last Modified: Wed, 28 Jan 2026 18:06:55 GMT  
		Size: 18.0 KB (17961 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.4.1602` - linux; ppc64le

```console
$ docker pull clojure@sha256:0ad403141c9e67d3bda30e7de5ea56340c2d78f585fd7fcb9c09fcae607f8104
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.9 MB (230926028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6f33f7e318b15379e69240bb6a02132738546de1b941b49de0e52ee26fbdca3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1768176000'
# Wed, 28 Jan 2026 18:00:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:00:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:00:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:00:33 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:00:33 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:32:55 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:32:55 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:32:55 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 28 Jan 2026 18:32:55 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 28 Jan 2026 18:32:55 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7fcf9f2b462d6af06c3ad2420b999e6b092984c4723ebac480c428a5d837d3b7`  
		Last Modified: Tue, 13 Jan 2026 00:40:14 GMT  
		Size: 52.3 MB (52327376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:339fa589af2d7cc446e03d21ea40f1e5c774818b048bcf7c10ea2c7201d72d8d`  
		Last Modified: Wed, 28 Jan 2026 18:02:31 GMT  
		Size: 91.6 MB (91610788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636b5d66deab728a4f82924ba403275ebdc53d6c24ed94b8cfbf95f5cdec73b3`  
		Last Modified: Wed, 28 Jan 2026 18:33:34 GMT  
		Size: 87.0 MB (86986822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5963dd44626248d2bb78f98d53c874214ddb17e630572ad03ef2a9ddcf9401ff`  
		Last Modified: Wed, 28 Jan 2026 18:33:31 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc150ea611541ce340cc11f540826379cb234b11346be0819d6b6a062a6dd498`  
		Last Modified: Wed, 28 Jan 2026 18:33:31 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1602` - unknown; unknown

```console
$ docker pull clojure@sha256:89578aad67bb1eba44ff941b8d7b18fcd61480fdf32418751a8aea1584d40680
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7352603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0716c75a4e9291f5fa1df35fc5ed50874168f2c9336ebaa3e5bd46e929f3ae2`

```dockerfile
```

-	Layers:
	-	`sha256:b160c47f52896ca0a163980bc9a4ec99fb4646ed322607821c81a8cdac28223e`  
		Last Modified: Wed, 28 Jan 2026 18:33:32 GMT  
		Size: 7.3 MB (7334749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c48eaf337a9e2bca96b37cbd192ffafb92ba8349491be732a2f68f0107f223d8`  
		Last Modified: Wed, 28 Jan 2026 18:33:31 GMT  
		Size: 17.9 KB (17854 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.4.1602` - linux; s390x

```console
$ docker pull clojure@sha256:0f98e854fdcd2e592b1a226e4c72c0ed52b82523d0900a58f31c4038f96cbe2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.3 MB (215313282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29779fa7d835e9cb234b25358e3ee4b11e79b50fe75e5d0712da7e0a26e413a8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1768176000'
# Thu, 15 Jan 2026 23:23:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 23:23:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 15 Jan 2026 23:23:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 23:23:06 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 15 Jan 2026 23:23:06 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:14:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:14:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:14:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 28 Jan 2026 18:14:33 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 28 Jan 2026 18:14:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:533e1723f6efd3a2dac5ef2d710062f1e6292bf061b83d41b908fe862b8922dc`  
		Last Modified: Tue, 13 Jan 2026 00:40:05 GMT  
		Size: 47.1 MB (47138430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d228a424ac43e5b633b49f78829dd5efa41560a237d73954164bfe619c713508`  
		Last Modified: Thu, 15 Jan 2026 23:23:50 GMT  
		Size: 88.2 MB (88210666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b0ba9d9d3854dd47092b9e5b65c186c20f0ca12abff1b35742597385dd377eb`  
		Last Modified: Wed, 28 Jan 2026 18:15:00 GMT  
		Size: 80.0 MB (79963145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc5edd8560096022eb70c77aab4ae705857bfea8665e069766f96a7046ec8946`  
		Last Modified: Wed, 28 Jan 2026 18:14:58 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fae78c6d0f943ffb8f8bd7f2a1e0f7ad6f6324aca340e185e0fe0813b6bbbf7`  
		Last Modified: Wed, 28 Jan 2026 18:14:58 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1602` - unknown; unknown

```console
$ docker pull clojure@sha256:e786eae477e71b447c7b3d4a8de624bd76368cc2bb348ab0412679ee4b27c711
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7339837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7d17ca7e34ee631fb3a81ad3a80647dc4de349dfdba570542155c1e2d959eac`

```dockerfile
```

-	Layers:
	-	`sha256:7e7fa150cd07b8901b740e8f0ba5bc498c075888cb7da0197e295f70b4b4c3bb`  
		Last Modified: Wed, 28 Jan 2026 18:14:58 GMT  
		Size: 7.3 MB (7322066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5a76d93a0970e051904c85e571be4619f55902978d5e6a27b0d95f6e12c6b20`  
		Last Modified: Wed, 28 Jan 2026 18:14:58 GMT  
		Size: 17.8 KB (17771 bytes)  
		MIME: application/vnd.in-toto+json
