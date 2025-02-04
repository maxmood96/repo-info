## `clojure:temurin-17-tools-deps-1.12.0.1501-bookworm`

```console
$ docker pull clojure@sha256:41229a4f8d19ccfd068841c259441b5d9200440a5581fd51e6ba4bae914021ee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.0.1501-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:6007ae82e1d5b519a267708cb6f347462e0a6fd2cb17361988ab0b42b3cd7cbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.0 MB (274040640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eac3b662ce81676a08680157840864ee8d6911be872c7ae352dca6b09e2d69a8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 29 Jan 2025 19:11:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
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
	-	`sha256:a492eee5e55976c7d3feecce4c564aaf6f14fb07fdc5019d06f4154eddc93fde`  
		Last Modified: Tue, 04 Feb 2025 01:36:22 GMT  
		Size: 48.5 MB (48479687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dea58b7264f17ce5191bbe0e99cb4796e1348485afaaacad15a001210e699b97`  
		Last Modified: Tue, 04 Feb 2025 05:21:25 GMT  
		Size: 144.6 MB (144566550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f96c97cff4099c1fddf79e381ede706add355863d33e81e47993e6b6869673`  
		Last Modified: Tue, 04 Feb 2025 05:21:21 GMT  
		Size: 81.0 MB (80993363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:797c6c36839c665383894b642599f5dc7db78f4bede706147885f6cb7140616f`  
		Last Modified: Tue, 04 Feb 2025 05:21:20 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:523e3c7e786ec7c051a70f853d4348c816cf82470d1ededce5c49b58a255aa38`  
		Last Modified: Tue, 04 Feb 2025 05:21:20 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1501-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:fea94856ff506d3580adf1d55dddf91463ece182c553da80664d8f8f17a90c41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7186899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43cad14d53ff96c2b3ed34453d45c19bf2e311f16878d14b4df88d076c0a0bd2`

```dockerfile
```

-	Layers:
	-	`sha256:54e1048455c19c7c62371b43c69730b3c55116dea7f39712dcaa9dbb54e957fa`  
		Last Modified: Tue, 04 Feb 2025 05:21:21 GMT  
		Size: 7.2 MB (7171078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5789678b6f9bcea2ef4675b09a04c77506d712a66595e3a7e424700d92f1e66`  
		Last Modified: Tue, 04 Feb 2025 05:21:20 GMT  
		Size: 15.8 KB (15821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.0.1501-bookworm` - linux; arm64 variant v8

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

### `clojure:temurin-17-tools-deps-1.12.0.1501-bookworm` - unknown; unknown

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
