## `clojure:temurin-11-bookworm-slim`

```console
$ docker pull clojure@sha256:492807d477e66371c6c99c833ff7803bc30f2df6a932421a4c8f95a6fd15e008
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

### `clojure:temurin-11-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:c8a9518ecdabfaeb941c0f6321420eadcf98f8adfc22098ed6d4153b37502ae3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.7 MB (243742851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0ca2bff7a5e606615cec864c9dc7a8c3bf009d88381fc4fd2740c47212f6118`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Wed, 15 Apr 2026 22:02:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:02:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:02:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:02:42 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:02:42 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:02:56 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:02:56 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:02:56 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:da539b6761059a0a114c6671f1267b57445e3a54da023db5c28be019e40f0284`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.2 MB (28236332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b3cfa662fa234719df3f2565822c6792eb79a9321162173858b92399ee9e065`  
		Last Modified: Wed, 15 Apr 2026 22:03:18 GMT  
		Size: 145.8 MB (145806794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da6908f73afce1208af2e54ab620a342c24082369ef4d460c51e763fe9c01ca`  
		Last Modified: Wed, 15 Apr 2026 22:03:16 GMT  
		Size: 69.7 MB (69699080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7c2370e5f410505c0909a4d71a6a0232944e33867625a3776878b1ec1dc0d49`  
		Last Modified: Wed, 15 Apr 2026 22:03:13 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2fffc19141c13cc625cda1b236faa299f596fbb933b2eec288814379dd62f358
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5150575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:957e33b193126128dc205948927008a74b657292a90236cb011a429d3259615b`

```dockerfile
```

-	Layers:
	-	`sha256:1ba370c1f4cef414e39a51da1008d0becc5ede014f8596ac589fe5a1caafb2ce`  
		Last Modified: Wed, 15 Apr 2026 22:03:13 GMT  
		Size: 5.1 MB (5136308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ee9fefff295157ffb0dd22729d97341d307c725a9015c5279dbf309f285d92f`  
		Last Modified: Wed, 15 Apr 2026 22:03:13 GMT  
		Size: 14.3 KB (14267 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e514a1bbd9d3e8087bee086d03c801aab06222157b4692a92c425b3a338b2740
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.3 MB (240309615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25206fc4db2eb6fd3ff6fdf3278cd269ff04f2e2551abb8d76fcc3cb6d556209`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Wed, 15 Apr 2026 22:14:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:14:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:14:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:14:08 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:14:08 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:14:24 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:14:24 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:14:24 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1dbbb2db815c2527e90ef5a3e4dfb957cfe7b61b6a7fc59722f1f64b1a1b611e`  
		Last Modified: Tue, 07 Apr 2026 00:10:39 GMT  
		Size: 28.1 MB (28116166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7e9b83acaffff7228e1828a6ce1b24e3827377398036667b135ab610132e28e`  
		Last Modified: Wed, 15 Apr 2026 22:14:47 GMT  
		Size: 142.5 MB (142500803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e18e4a8e8f69320d3eb49323880c4aab9a197b621e57429f6ce30ebac5381900`  
		Last Modified: Wed, 15 Apr 2026 22:14:46 GMT  
		Size: 69.7 MB (69692001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac8e538cf3a83c0f4415e7aa4076b60fe8aa484c11c3057dafbeda4e89fbd1c0`  
		Last Modified: Wed, 15 Apr 2026 22:14:43 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:72749f1f845273b03a8e3aca15c58cf0d1796341ddf172fa7f27cc22df7f1d66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5157072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecf5046b6c4fdb303c46b46261844eeb02a040c0a1ccf6e0d3fc395527920165`

```dockerfile
```

-	Layers:
	-	`sha256:92ecf9d95b229a6cc4d57aec1058ac8b6e5be3fce71fab95c129054702a2aa8d`  
		Last Modified: Wed, 15 Apr 2026 22:14:43 GMT  
		Size: 5.1 MB (5142687 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a617450c9f6ffcf1ff7e9576c624d6b18bb3049cb07caa7d51d9bd9e5c2482e`  
		Last Modified: Wed, 15 Apr 2026 22:14:42 GMT  
		Size: 14.4 KB (14385 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:b9f9d0d0a8db3d9d5c3b9458a2ad43c79224489155c1bb00cba9efc1fadc4e25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.6 MB (240610680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15ccca3eb0c1cbb045c191db1bad1b91895eb8f3f43a69ba6a5a612ea5644286`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 14:30:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 14:30:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 14:30:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 14:30:20 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 14:30:21 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 14:34:23 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 14:34:24 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 14:34:24 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b1c56220ca211bc9d02f1ed5c589465809676b6ab2cef705f1e2fb8e9726de76`  
		Last Modified: Tue, 07 Apr 2026 00:09:42 GMT  
		Size: 32.1 MB (32078464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3239a667025d854bea5c185db151e78d7d54c70792c78737dc5abe529056f1e3`  
		Last Modified: Tue, 07 Apr 2026 14:31:37 GMT  
		Size: 133.0 MB (132997659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:131d481b68baa3fec27d647f52eabdb66eef0094c76b38600716eb65dcceccb0`  
		Last Modified: Tue, 07 Apr 2026 14:34:59 GMT  
		Size: 75.5 MB (75533910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d03a597402001ff881964fb3cb24301ce1fe43336b6d3baff2810fdd2e582b9`  
		Last Modified: Tue, 07 Apr 2026 14:34:57 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:19d177d0af146bb66a71a58d1dffdf3cdf500a648aa14ef7df776b621efc6eb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5155166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99d0499ec78be5cf6cce806a4aa5b00b8169fd231a1fae3c383daa539c83c552`

```dockerfile
```

-	Layers:
	-	`sha256:66f34b38bc056cda2a86aa081c7f4cef5a0e2e55e65f32da1f2acf60921ee095`  
		Last Modified: Tue, 07 Apr 2026 14:34:57 GMT  
		Size: 5.1 MB (5140851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:675f723318e6e1ee53eaa12b0101eed93972297e6d133a31de2a57d16303eb6a`  
		Last Modified: Tue, 07 Apr 2026 14:34:56 GMT  
		Size: 14.3 KB (14315 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:fe3514d027d4e1e8a3a0c28fd4bf457693c3ed910193f0a769de42c67925f239
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.0 MB (221968099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be71905062eeb99cfc2de3036e7d71a343eb7704f8263c6084ef2de23a110696`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 05:39:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 05:39:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 05:39:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 05:39:16 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 05:39:17 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 05:40:28 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 05:40:28 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 05:40:28 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:c23087fbbda0d8352ee6b2d159c503459acb89da0eba1729b411ca394e68e292`  
		Last Modified: Tue, 07 Apr 2026 00:10:59 GMT  
		Size: 26.9 MB (26891634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22e385f726bab54d70ecc51bad16d60533bc9b6d182b632879bc3c86a7da9d89`  
		Last Modified: Tue, 07 Apr 2026 05:39:56 GMT  
		Size: 126.6 MB (126562190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e7eb79f05f084698548b1b10f8a4ecd434f5d5c2821d46998b074a17e5361b`  
		Last Modified: Tue, 07 Apr 2026 05:40:52 GMT  
		Size: 68.5 MB (68513630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:798fabeb47c2a9d9c1c3aba63ff4b02fb5c5a8c4f4647e4d1c32976bc74f9bb1`  
		Last Modified: Tue, 07 Apr 2026 05:40:51 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:055c94a0a784c1ce4da1c215c168b0e7dbd439080b5cdb1040ef90d8f6722471
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5141900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3c5dd4c10e0a745b5106033f547ee128b2cbbf98fc9b1d5609018ea3e92fabb`

```dockerfile
```

-	Layers:
	-	`sha256:ca57aaaf7510edcc5983c73d136f36cc142a1ca2b96b326a045da3d8bcc78de7`  
		Last Modified: Tue, 07 Apr 2026 05:40:51 GMT  
		Size: 5.1 MB (5127633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da4aabab24801f056ffc696b5bf463701ed8c1d02bd704212a6b3800931971d6`  
		Last Modified: Tue, 07 Apr 2026 05:40:51 GMT  
		Size: 14.3 KB (14267 bytes)  
		MIME: application/vnd.in-toto+json
