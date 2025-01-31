## `clojure:temurin-17-bookworm`

```console
$ docker pull clojure@sha256:a81176581f236d64e33e330c21b29bece44d4b13a555e627f5cc621a347e1c4b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:5e23f400d5c85b378471c16b5390404ed7273bdd5dc6fe225a78020f2fb2f71e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.0 MB (274041402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:734a3319e5ff7996780994f7d9fc86d375fe07dda9a1628e2ed0c09c9ba94c1c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Wed, 29 Jan 2025 19:11:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Jan 2025 19:11:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jan 2025 19:11:46 GMT
ENV CLOJURE_VERSION=1.12.0.1501
# Wed, 29 Jan 2025 19:11:46 GMT
WORKDIR /tmp
# Wed, 29 Jan 2025 19:11:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "65257085958376a3c89755a6108d67163882c75af709fe8c8918222ca5730aef *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 29 Jan 2025 19:11:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:fd0410a2d1aece5360035b61b0a60d8d6ce56badb9d30a5c86113b3ec724f72a`  
		Last Modified: Tue, 14 Jan 2025 01:33:18 GMT  
		Size: 48.5 MB (48479962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8001366c727ddda1b24b74931277d0f601c16abd3b056cebec8c1ecb15aa7e4`  
		Last Modified: Fri, 31 Jan 2025 02:17:58 GMT  
		Size: 144.6 MB (144566554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b42539bb121a5bf132426851dc0d5e7a9410b528f1d85b2598f52b9d72aaa5c0`  
		Last Modified: Fri, 31 Jan 2025 02:17:57 GMT  
		Size: 81.0 MB (80993846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0472efaf124fc50b0e0882400b32e7b9c167a79e7e6aa06651ca22327f343827`  
		Last Modified: Fri, 31 Jan 2025 02:17:56 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3013d425cf05248c649a1d7adb0994561d0b964228421d5d206200f27db3fc3`  
		Last Modified: Fri, 31 Jan 2025 02:17:56 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:ad8884982c8663cca3dcf60f635ef91ac9ccd8db941bfded35490671e32010fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7186899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8865b0be7336db528933b9cda35f9c173f19c0f1274473c373f5c9906a317cd1`

```dockerfile
```

-	Layers:
	-	`sha256:fd1f01ddc947d355e031fd8f87cbceb3b267d902437d029f793025ef3ed79bbb`  
		Last Modified: Fri, 31 Jan 2025 02:17:56 GMT  
		Size: 7.2 MB (7171078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9dc829b93a1a4c56a1e6f7dc3197f6577c792556f70fa02b0e48b292fc7f8d3c`  
		Last Modified: Fri, 31 Jan 2025 02:17:56 GMT  
		Size: 15.8 KB (15821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:990789b2941ba458e52024570a7bb571c74269522fcba980eacd22637bb0678b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.6 MB (272608473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78c48766a33a4b0820ad7038940ee2af6e610cf0ad1757ada68c63cec04b7845`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Wed, 29 Jan 2025 19:11:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Jan 2025 19:11:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jan 2025 19:11:46 GMT
ENV CLOJURE_VERSION=1.12.0.1501
# Wed, 29 Jan 2025 19:11:46 GMT
WORKDIR /tmp
# Wed, 29 Jan 2025 19:11:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "65257085958376a3c89755a6108d67163882c75af709fe8c8918222ca5730aef *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 29 Jan 2025 19:11:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e474a4a4cbbfe5b308416796d99b79605bbfad6cb32ab1d94d61dc0585a907ea`  
		Last Modified: Tue, 14 Jan 2025 01:35:41 GMT  
		Size: 48.3 MB (48306896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c44843f4ea9650b9e13725987fa85f7a87043276b74817da92ea84df014b11a2`  
		Last Modified: Fri, 31 Jan 2025 05:10:16 GMT  
		Size: 143.5 MB (143454587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c4c96c6059e815ca3e0145b5e43e9f42ea8f978ac0fd7d2e1c9dde1f4f3cf7`  
		Last Modified: Fri, 31 Jan 2025 05:15:20 GMT  
		Size: 80.8 MB (80845948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0bebfbcdc542e0f89e14c42fa87e75cc51a008b46bf2980b9ddad1a007ea28`  
		Last Modified: Fri, 31 Jan 2025 05:15:17 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918cce9069f4f576e0770eb259037d99db4768c04a777cc7919f71ac04a4a47a`  
		Last Modified: Fri, 31 Jan 2025 05:15:17 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:471e1b42d0cc7eec48bc6148f59d91f94f9dcccfab2ac34b499aa1a92d0ff394
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7192779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69a096f8b03e1a150859d55c031c9aa685a7031051955f1c8671311f752fb83b`

```dockerfile
```

-	Layers:
	-	`sha256:507c619ddb955ddbaf34e9c3213a49f0cc5e628f63802145fd4314e29a9a3aec`  
		Last Modified: Fri, 31 Jan 2025 05:15:18 GMT  
		Size: 7.2 MB (7176841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:972fff6feaaad853b3c09bbf42c3f23fd9525cfc32051f200b6285fa1d82bb2b`  
		Last Modified: Fri, 31 Jan 2025 05:15:17 GMT  
		Size: 15.9 KB (15938 bytes)  
		MIME: application/vnd.in-toto+json
