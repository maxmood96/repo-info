## `clojure:temurin-8-bookworm`

```console
$ docker pull clojure@sha256:e2d7e335829aa50f918249b5468421dc6568fed8c18a0ecdb84a716648e78b27
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:4f96206f1ae3ca1faa9ce28bde755ce1b9c47dd80405efa9a14173d1ac328109
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.8 MB (181819905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afe3bdd9d3c088025ebe1ac7b69a1900a088627b79cd106f9807ed387827286e`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Thu, 04 Jun 2026 17:39:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:39:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:39:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:39:35 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:39:35 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:39:50 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:39:50 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:39:50 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:4887723d153cfd7fd9e356c8730311c36a64e4f9329f9d3ae1929e05715f2e73`  
		Last Modified: Tue, 19 May 2026 22:36:12 GMT  
		Size: 48.5 MB (48495432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57d6688c4cb6a8dcd4e43995a545d93213191460afb7ac8ac9f85cca912c2a45`  
		Last Modified: Thu, 04 Jun 2026 17:40:10 GMT  
		Size: 55.2 MB (55198725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54d7ad99ef4e9d2d9fa778d3d98dad69a024e35d7631f9c2866119eb2c334040`  
		Last Modified: Thu, 04 Jun 2026 17:40:10 GMT  
		Size: 78.1 MB (78125103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:379e22387acd4fad547f6b0147a0f77a00e6ba92bfa3dd473b6c7108ffd344fd`  
		Last Modified: Thu, 04 Jun 2026 17:40:07 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:099a2229d3039b7f6f5023016268eff828f3190be0cff25442e933d74673b97e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7510824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b68b191bab18e3dc294ef3c7676b6aa610de856ac0df7b0c531c361fd995328`

```dockerfile
```

-	Layers:
	-	`sha256:8504c1ba907d74893802460d7132ea364cded280c1fc512ea1c372f1f376b1dc`  
		Last Modified: Thu, 04 Jun 2026 17:40:07 GMT  
		Size: 7.5 MB (7496476 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e60dcdf891f9fc1b1a51568adc86f298c0221a52c4b87d065d014c4f4a54919f`  
		Last Modified: Thu, 04 Jun 2026 17:40:07 GMT  
		Size: 14.3 KB (14348 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3cd350ee1150e1392558a75a2023e87bf55a8960ca9b804d115fd7b9dbc8fc93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.8 MB (180774646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55f060406472545c46dc2dbdabb6bfcceda2600493af5c79084049d3068fd556`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Thu, 04 Jun 2026 17:40:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:40:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:40:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:40:13 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:40:13 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:40:27 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:40:28 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:40:28 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1fbcdab7270278c1f989ae72190255d85d2117e990efb76cde6eb206b803672c`  
		Last Modified: Tue, 19 May 2026 22:36:02 GMT  
		Size: 48.4 MB (48379432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b4de670789f92b2b287b948e80429a16249ed6b6d011ce20e334ad3135d509b`  
		Last Modified: Thu, 04 Jun 2026 17:40:46 GMT  
		Size: 54.3 MB (54272936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57522baa4fccd195ef8eac32907a5dcc555309a6b6cb7e84982f02a1b48e5c93`  
		Last Modified: Thu, 04 Jun 2026 17:40:47 GMT  
		Size: 78.1 MB (78121633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a35a8c60efc1cd9eefe2934fbbfa11eb30996d43d31ffdffc6a0590cec882c5`  
		Last Modified: Thu, 04 Jun 2026 17:40:44 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:51e7ca7abf3379da9fcce2e066ed6e3691ebd0f3050232ee05716c1561f339b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7517405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2145419618ef1009c2fd8547826561eb5994b63b784b0eeec3b43096a0160556`

```dockerfile
```

-	Layers:
	-	`sha256:195d4cef1bd9966fa2da229852143573b776470da6c50f921cde464225dd8a2a`  
		Last Modified: Thu, 04 Jun 2026 17:40:44 GMT  
		Size: 7.5 MB (7502939 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:360b3f546f07812ff3b0f13cd8417348f79e88927d5179e46c1744d970ec9234`  
		Last Modified: Thu, 04 Jun 2026 17:40:44 GMT  
		Size: 14.5 KB (14466 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:8bc9888055e31895460f60ca958f16f9b9025617411de81f3499946702911e52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.0 MB (188969443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19a2a7ee09c1ac8d0164bffc506db33a6f8faaa4267e080553f205031bb3abea`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1779062400'
# Thu, 04 Jun 2026 17:40:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:40:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:40:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:40:22 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:40:22 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:41:08 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:41:08 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:41:08 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b3943e183051423c3dc79fa53ad6d50fff9621945bbfc636eec039b14ead2b66`  
		Last Modified: Tue, 19 May 2026 22:35:10 GMT  
		Size: 52.3 MB (52340199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9545e2d4ebda8e55ef145d34e6940ac7e7ccc363d399c876eb386ef6e83d1ef7`  
		Last Modified: Thu, 04 Jun 2026 17:41:54 GMT  
		Size: 52.7 MB (52669123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34df4fe7cff9f4bb8570ba9add428323c9bbcf3cb37cac931fb0b0c031895c15`  
		Last Modified: Thu, 04 Jun 2026 17:41:54 GMT  
		Size: 84.0 MB (83959473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6294bebc27a3bcad8da12343b8d0112d92a4c50118efb0e157138b4bc4a970e7`  
		Last Modified: Thu, 04 Jun 2026 17:41:51 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:c8d22af830b74741ea8a63b6a4c648b1264235f014ab2eef5c35e6d0a963f3b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7516683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:213322bc4d3c85f166e08d2e2ca0f3c0cbc3c89d46bcac66f5000f332e49fb87`

```dockerfile
```

-	Layers:
	-	`sha256:8c8fec3827d04fae1be5dfb06131099bdeb806d176ee481d88d8d25ce095f47e`  
		Last Modified: Thu, 04 Jun 2026 17:41:52 GMT  
		Size: 7.5 MB (7502287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d45345172fed7ee781210f98d3c33673eb28083bbbe28bbe380ee9c8cb10e3a`  
		Last Modified: Thu, 04 Jun 2026 17:41:51 GMT  
		Size: 14.4 KB (14396 bytes)  
		MIME: application/vnd.in-toto+json
