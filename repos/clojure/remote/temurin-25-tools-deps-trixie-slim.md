## `clojure:temurin-25-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:52b3e586b3bec1908ce4644ca0b41623ef4d327e38422e3ec12f0cdf724b7d7b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-25-tools-deps-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:313aa81a7a725d86e3bea4609d81bf0ef9deb1bfb2c001079055347d8fa77dd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.4 MB (194367054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0fa2293e4c79570bf11775e63d6fa17a4cba735a1b0fe13796847bc4a5ebe66`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Fri, 08 May 2026 00:16:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:16:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:16:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:16:03 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 00:28:28 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:28:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 00:28:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 00:28:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:28:46 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:28:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38c45c777ee90963edc351ae24e3c7a190e5043aa33c4f959347a3c868b46dd7`  
		Last Modified: Fri, 08 May 2026 00:16:53 GMT  
		Size: 92.6 MB (92574578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38db179254291357cd7c371193934704472506574495dd0b8a750f973251c474`  
		Last Modified: Fri, 08 May 2026 00:29:04 GMT  
		Size: 72.0 MB (72011264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ad95d29c6ad15a8813dec133da3ef790213548ebbe98625340edc0632ed1098`  
		Last Modified: Fri, 08 May 2026 00:29:01 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016fa13e006dd1006d52fa9e1b5e03df6db213a6197cf0da0ee45c8fc84161ec`  
		Last Modified: Fri, 08 May 2026 00:29:01 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:064a6e44d486a0ad42d0d2327ac143b181840497a02d13a540b72e3a0186adac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5244548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd9ec2a0ebed14bfbd76c23663bd422ff3d27f8a71829687c4864c90ff3490e3`

```dockerfile
```

-	Layers:
	-	`sha256:d9e296d565d2271714526a6bf19404ed8489655df5462072fd7b9cb3e4d6f0bd`  
		Last Modified: Fri, 08 May 2026 00:29:01 GMT  
		Size: 5.2 MB (5227901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea4194ac96009fe5eeabdb948d4928f5a51031a3068c2ac2d78ecdca490bb4bd`  
		Last Modified: Fri, 08 May 2026 00:29:01 GMT  
		Size: 16.6 KB (16647 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d5aeac36eea918b7dfcf9dd3c6d9f88002c57f8fdfe68d588652fa4b6ae64929
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.5 MB (193518362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:222d384d4aed56cb8c484071b44c43499104895694cbd5178bdaf3c3c050aebe`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Fri, 08 May 2026 00:28:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:28:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:28:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:28:02 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 00:28:02 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:28:19 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 00:28:19 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 00:28:19 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:28:19 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:28:19 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c71ea4d943928683c1373ba3215d8c5f21d0093e3d3d06b5a624e5cb50494234`  
		Last Modified: Fri, 08 May 2026 00:28:41 GMT  
		Size: 91.5 MB (91542279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0086c5676fb720c48a0c9e732af4c9743a77c46bb57f621c1f2f2118788cd62`  
		Last Modified: Fri, 08 May 2026 00:28:39 GMT  
		Size: 71.8 MB (71831437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ad05748641368d52919963cc392dcc76cf9ac3e306d994a5e68f6b676c73f94`  
		Last Modified: Fri, 08 May 2026 00:28:37 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90bc4ea19a59f048685aac31aa7d6e5ca933dc8fef2ad00775df15974b6e2399`  
		Last Modified: Fri, 08 May 2026 00:28:37 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3119b9ace0b2306b095290fc61fc71c6d2f2110eba024f1278614070133ced56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5250480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dd3d7a53d872c44a3a2766ed6ef10795de2cf5cf1e813ee9af39cfe3e7c22ae`

```dockerfile
```

-	Layers:
	-	`sha256:d3f8bdbe2cf5557c03057ec26abe7c4fdb92c9093f040989a7f3e796a24fb2c3`  
		Last Modified: Fri, 08 May 2026 00:28:37 GMT  
		Size: 5.2 MB (5233691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:acc352597ae95c7e52c52bf9317ed284b28b6a2180c3c2a81d0d890fdfafc5cb`  
		Last Modified: Fri, 08 May 2026 00:28:37 GMT  
		Size: 16.8 KB (16789 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:6ddca13275531b5a558b048cd887ce749fbe6e14d297ea5c69ca0aa042755744
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.9 MB (202942056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bbcf211994da88f2edea834a73c1e59a2e8e410900393edfde86a90c15d2363`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Fri, 08 May 2026 01:45:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 01:45:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 01:45:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 01:45:30 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 01:45:30 GMT
WORKDIR /tmp
# Fri, 08 May 2026 01:50:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 01:50:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 01:50:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 01:50:11 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 01:50:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b5fd051d0fcd0789e7358cba300f83befdba943416041497be86050e282a6d02`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 33.6 MB (33598032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e50e227b32fab760ab734a722d523335c702357014ac0ce34693e4421965f3b9`  
		Last Modified: Fri, 08 May 2026 01:49:25 GMT  
		Size: 91.9 MB (91914037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b073b09e7c941cf14ee3cad0b02823b3f28209dc3d93108b91944e272aa1021c`  
		Last Modified: Fri, 08 May 2026 01:50:45 GMT  
		Size: 77.4 MB (77428947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18e2125a0d36edaab906cb22c591dd50c82fa5558013f231c537dfd0b4c2cb26`  
		Last Modified: Fri, 08 May 2026 01:50:42 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f241b78d96c9fe2e639e41ec9048e954c3f79519ee9915bd04238fd564ed1d33`  
		Last Modified: Fri, 08 May 2026 01:50:42 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:cedead179625d1415dee750f3b63275b4d148f02f4c90c357c5a9dbfa3de7bbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5232302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6a4b66b5cf6178eaa07208d97a383db7de8418e38d7aeb88cdb9296bf2899fe`

```dockerfile
```

-	Layers:
	-	`sha256:07b3cd3b41c80cfbc9e3271549197b57e2dd2678bc4d36ed696556d279aba8f8`  
		Last Modified: Fri, 08 May 2026 01:50:42 GMT  
		Size: 5.2 MB (5215596 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a111d1f27ef0cc694f7e15a48afdb8ba30460431030f025203187495dd29df13`  
		Last Modified: Fri, 08 May 2026 01:50:42 GMT  
		Size: 16.7 KB (16706 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:be89d0af9b54d14061ba4963cf632c0abdeebf260743bbc63cf55dc9852cfa3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.2 MB (190196910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fa21e97ea281844cdcea1fbc02f616d0e17dcda82be06e225d98d1fcc0e91bc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Fri, 01 May 2026 01:17:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 May 2026 01:17:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 01 May 2026 01:17:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 May 2026 01:17:25 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 01 May 2026 01:17:25 GMT
WORKDIR /tmp
# Fri, 01 May 2026 01:40:01 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 01 May 2026 01:40:01 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 01 May 2026 01:40:01 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 01 May 2026 01:40:01 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 01 May 2026 01:40:01 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c59e3a1f334be9f0528643dd07d69319f75f877f83be33ec1eff872a489985a0`  
		Last Modified: Wed, 22 Apr 2026 02:30:51 GMT  
		Size: 28.3 MB (28280195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a463537893b115e8f6bf5847dfb28b93d1015ffeaba8f0acf52e10133dfcf3`  
		Last Modified: Fri, 01 May 2026 01:22:48 GMT  
		Size: 91.0 MB (91014937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:189637ec0b992e6712b62b6fb4f7b70346d8d5bcb3ee094fd4aab889fff4c37f`  
		Last Modified: Fri, 01 May 2026 01:43:39 GMT  
		Size: 70.9 MB (70900737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79eaea740b68965c8fdc3649064b2c913832c335f630b9ba2a8384fb8106320d`  
		Last Modified: Fri, 01 May 2026 01:43:28 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40e977049073a11f7f44c386d34f63afc5a55ee22fb7bc04268acd8cc3aca264`  
		Last Modified: Fri, 01 May 2026 01:43:28 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e91e0fd693ca996b99de0cbe7c0cd9858b0a648a250235e9c08fd4549071b198
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5215940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a6965907ae999b8e0337c662e8c9772925e92bfc1a659806cc6fa700e443fec`

```dockerfile
```

-	Layers:
	-	`sha256:cbd087a5706682fae7db02ce8143c7d1f9e49a1a746c6749c8ab1d763063d0f0`  
		Last Modified: Fri, 01 May 2026 01:43:29 GMT  
		Size: 5.2 MB (5199388 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b976013de3d9592c571721b84f129ce8eee150012ccf55a24491e0511d7c0ff9`  
		Last Modified: Fri, 01 May 2026 01:43:28 GMT  
		Size: 16.6 KB (16552 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:9c2502e5123eb51e236495e5e87213e3bb3494b580080f9061a43c9a2bc0f196
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.2 MB (191248936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:308b9018ea73962501cda5455ba58a51f551c9b093f031c8e0a49d0f02c3a835`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Thu, 30 Apr 2026 23:50:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Apr 2026 23:50:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 30 Apr 2026 23:50:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:50:52 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 30 Apr 2026 23:50:52 GMT
WORKDIR /tmp
# Thu, 30 Apr 2026 23:52:25 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 30 Apr 2026 23:52:25 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 30 Apr 2026 23:52:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 30 Apr 2026 23:52:26 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 30 Apr 2026 23:52:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:71574deb335f1e823f938f4a215de00a90d63866898f1f354a0b15e8b9c30577`  
		Last Modified: Wed, 22 Apr 2026 00:17:08 GMT  
		Size: 29.8 MB (29840300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72ee46c033b5990060b9acaa5985a11a008290bfbbb27b32d546e2487a9a5e65`  
		Last Modified: Thu, 30 Apr 2026 23:51:37 GMT  
		Size: 88.4 MB (88420341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5e365ad6b822f0672f587fe0ca1d8b89f990afac4d0c85f9c7afebcfe18e3e`  
		Last Modified: Thu, 30 Apr 2026 23:52:51 GMT  
		Size: 73.0 MB (72987256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5fe71a76bb2069146a4a26d7785b09f888bb67b1f3163c902cd9f47dccd389f`  
		Last Modified: Thu, 30 Apr 2026 23:52:50 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e07eb1e7e55a0a5df4833db4f1b84d4cd77acb8cf49fe0c4b7ccb2c4ee1421f`  
		Last Modified: Thu, 30 Apr 2026 23:52:50 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:81205a565dcd6b011c88ecc5e09bf025c257c6b74864e1e44d5bcefd53b195cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5225034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:348345c168cf5d68b6251f5d9bbe790f4a6aa6044eb95441ada31348623e9b3f`

```dockerfile
```

-	Layers:
	-	`sha256:1dd35f60761400eccf048eb259698c231041f00d8ada4ba40e866614448e7c11`  
		Last Modified: Fri, 08 May 2026 00:41:25 GMT  
		Size: 5.2 MB (5208387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:092a257c90694a3a579a7074a08b0f52e513d787ee301e3edc216f4544ee2eac`  
		Last Modified: Fri, 08 May 2026 00:41:25 GMT  
		Size: 16.6 KB (16647 bytes)  
		MIME: application/vnd.in-toto+json
