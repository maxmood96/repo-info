## `clojure:temurin-17-bullseye`

```console
$ docker pull clojure@sha256:ca5cd0258ef663a0d067eb6ae8cb45d7c549f3635ebe13212c01a6bbf80c142a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:aa9c2c397c5bf37071b9bdac9f7e594110974b66b8ca20c1536f748b9256a4fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.9 MB (268927952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0f215df68982892ca3957350263f887bea6af7fa10d18dfe427cc10b710f039`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Tue, 17 Feb 2026 21:43:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:43:19 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:43:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:43:19 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 21:43:19 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:43:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 21:43:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 21:43:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 21:43:34 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 21:43:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4837b8a287e31893a57c67e4e7e49ea3681edb8424480549d8b5f5b29691313e`  
		Last Modified: Tue, 03 Feb 2026 01:13:50 GMT  
		Size: 53.8 MB (53756259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8570f7e08a9fa16efb956296bfa9ad41e35508c2edefcc4f31efeeb6be8e2044`  
		Last Modified: Tue, 17 Feb 2026 21:43:57 GMT  
		Size: 145.6 MB (145628753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d09a437d1f9947e49b4894104f63029c185079e6ea891b88d8509c1df3529c`  
		Last Modified: Tue, 17 Feb 2026 21:43:56 GMT  
		Size: 69.5 MB (69541895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c9246b75801f9198cd08f7a967e33edb4986479941790c6839c483cd8999749`  
		Last Modified: Tue, 17 Feb 2026 21:43:53 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdd6f8200e130065d6bf48f8865198858dfc1d2881cfff38212360f1af5f7371`  
		Last Modified: Tue, 17 Feb 2026 21:43:52 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:19569d0c43e224526754eb0251471688a63347afa8e19d878b638183ee6fb917
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7413498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5e644619f8b68c50870c17a20e1abe9cb874b4ae33c6d901cd03f1ab221ce1c`

```dockerfile
```

-	Layers:
	-	`sha256:b7171be427303de88443e2241fc1d6adf3fe662b2192f5dbf69d6d9af2331908`  
		Last Modified: Tue, 17 Feb 2026 21:43:53 GMT  
		Size: 7.4 MB (7397720 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a372197dcdb9ed4e883884e33dcbf5b92663da0d4612d61264e2093b2164f1a4`  
		Last Modified: Tue, 17 Feb 2026 21:43:52 GMT  
		Size: 15.8 KB (15778 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:774605bcb933ac80a3a4e464bcf07b35fdebf19e77e21409598b647cf68f6660
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266389189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a78bd62e7597911306a4bc393b01f771f83161f62f8b71860bbb5cba2fb07d4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1769990400'
# Tue, 17 Feb 2026 21:43:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:43:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:43:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:43:22 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 21:43:22 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:43:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 21:43:37 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 21:43:37 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 21:43:37 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 21:43:37 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0742c20cdb1eb0c212cefb0ff441553e29e6ccfa92b808cca3d7e8548a6fd569`  
		Last Modified: Tue, 03 Feb 2026 01:13:54 GMT  
		Size: 52.3 MB (52258320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330745f74a00c586d31ecf5a23f640b29eb94edfeb966ab54b61ef192ae1ab2b`  
		Last Modified: Tue, 17 Feb 2026 21:44:01 GMT  
		Size: 144.4 MB (144436241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d34d1a71cd2db3aa64b3be24d1c70fb962d830c53e43cd4bc9965e822c84bd5`  
		Last Modified: Tue, 17 Feb 2026 21:43:59 GMT  
		Size: 69.7 MB (69693587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5fd47e3f958d030d8f548dbee4ffe8065a79f6a7900ed808d31e11e83d0dd53`  
		Last Modified: Tue, 17 Feb 2026 21:43:57 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6599889e154188cae45e82cc323ea842e630fd85b37b74cd46af24ef01a1ec2b`  
		Last Modified: Tue, 17 Feb 2026 21:43:57 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:1ac2820646b0f2143055c7f091e61e3932bf64d5d5502714f2349ae358089e02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7418715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e63c5ff66904227b5999e8af07ef1b091e1faa7618ad33469fe9c89f16f66007`

```dockerfile
```

-	Layers:
	-	`sha256:09a3e685b0c876e36d5006a4eec5f054e1a8a745f1e0a3d86eaa7239e343bb04`  
		Last Modified: Tue, 17 Feb 2026 21:43:57 GMT  
		Size: 7.4 MB (7402819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c47b04ce6fb830126a9e87075909565e9386a9351eda0c057a3195b895b190b`  
		Last Modified: Tue, 17 Feb 2026 21:43:56 GMT  
		Size: 15.9 KB (15896 bytes)  
		MIME: application/vnd.in-toto+json
