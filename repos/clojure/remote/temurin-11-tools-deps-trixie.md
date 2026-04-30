## `clojure:temurin-11-tools-deps-trixie`

```console
$ docker pull clojure@sha256:bfadad85d0fbac6dec1f03d247150c29c5802b2c00aad9cfe34890eb43184ad3
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

### `clojure:temurin-11-tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:854a8adcb37e5f0785acfcf3ff53f403c00834479b8295ebaba933f0f692276e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.8 MB (280759644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f76468aadf9d3a26f8a70f601d280af45be6d9d275ccb45f00bab231324ca8d6`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 29 Apr 2026 23:15:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Apr 2026 23:15:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Apr 2026 23:15:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Apr 2026 23:15:27 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 29 Apr 2026 23:15:27 GMT
WORKDIR /tmp
# Wed, 29 Apr 2026 23:15:44 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 29 Apr 2026 23:15:44 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Apr 2026 23:15:44 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:3b32e3bb7338c216b077e95920ae53332d81bd57f4a7393bc324432d5a3f88a2`  
		Last Modified: Wed, 22 Apr 2026 00:16:56 GMT  
		Size: 49.3 MB (49302102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:290b1e3b89bfa0f587880a5ab7e531258fb1d2091c78aa659074d1b9f193506f`  
		Last Modified: Wed, 29 Apr 2026 23:16:11 GMT  
		Size: 145.9 MB (145886254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2be6e44fa9ec60df3ea4985b2bb73254b5baf4655302e93bddd8c0fc2e05686`  
		Last Modified: Wed, 29 Apr 2026 23:16:09 GMT  
		Size: 85.6 MB (85570644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c01b873a3f16d6b7585d7cbe35505b876b91f5de22df8a6f439f813710bebb2`  
		Last Modified: Wed, 29 Apr 2026 23:16:04 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:64664a0c94a3ae5b5ea457db86658ccbe79612faf3fa355a85e2a847b8c41837
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7505049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:617c8ad285751cc87082815f6db34c2c85c9269fd23066b1b87f69f78bbda545`

```dockerfile
```

-	Layers:
	-	`sha256:da68302a212747033aba81b9e286c66955137c6ebbaefee9be0a27b64bef3693`  
		Last Modified: Wed, 29 Apr 2026 23:16:04 GMT  
		Size: 7.5 MB (7490864 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85ac6d0946afef7c0cd2ca5c2254eb9cb469b8276889d7e92ffbc723eb27c4aa`  
		Last Modified: Wed, 29 Apr 2026 23:16:03 GMT  
		Size: 14.2 KB (14185 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1e728d92fe1efd74562c410a78ee58fa95485b9a1e702a503269fc8b78369f70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.6 MB (277637273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38af77561c47be1399af3d454a5623304d2a6140af05d882aac74a8d2a2409f7`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 29 Apr 2026 23:15:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Apr 2026 23:15:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Apr 2026 23:15:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Apr 2026 23:15:01 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 29 Apr 2026 23:15:02 GMT
WORKDIR /tmp
# Wed, 29 Apr 2026 23:15:21 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 29 Apr 2026 23:15:21 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Apr 2026 23:15:21 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:6e7932d5cb5573d1bff4fb8801baad19fc72d2ae741bb046333573653944f5a5`  
		Last Modified: Wed, 22 Apr 2026 00:16:45 GMT  
		Size: 49.7 MB (49669245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872c9c356c260dac332ff0b0043115fa2f46887172687637f4b905d8b21782a3`  
		Last Modified: Wed, 29 Apr 2026 23:15:49 GMT  
		Size: 142.6 MB (142583979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e8cd08c15b04e23b2f5b336517a7a1de1618c359086667fd93f51d075123521`  
		Last Modified: Wed, 29 Apr 2026 23:15:47 GMT  
		Size: 85.4 MB (85383406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c8a4d5d8c2d312d117bd6ddd6fd3e84600685933f685c2a762caeb67e3b1d1`  
		Last Modified: Wed, 29 Apr 2026 23:15:44 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:0a1f1e62d59607394c2ff421e6900f9433f829e53a07ffc075220b27ecd47266
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7512815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:379438b520b8bfc3e904fb555f50f23d4568c1a2a275347c93066260bfe0ce01`

```dockerfile
```

-	Layers:
	-	`sha256:c1f6641610dab6894c7ab4f36ec43a73be22f485e9cd678fb72a288b6bf2b7e1`  
		Last Modified: Wed, 29 Apr 2026 23:15:44 GMT  
		Size: 7.5 MB (7498512 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e6160d2dbfb102febec3a76cfbc31762da60b631ab1c2170b5793ae0c9178ee`  
		Last Modified: Wed, 29 Apr 2026 23:15:44 GMT  
		Size: 14.3 KB (14303 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:3d24ae3ec0c2086d2663bef8806c641d2b2f4180463c2627fcf6718113a56b87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.1 MB (277107470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1c0b39514be3966e74e04732fb4b150439cfb71919f6eea4dd2bb0f77ab90e7`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 08:22:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 08:22:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 08:22:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 08:22:31 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 08:22:35 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 08:27:43 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 08:27:43 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 08:27:43 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:0fab4f6170940889900b2327e1b3c62dace993eab8074ca7d33d1ffeef137c08`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 53.1 MB (53122984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3730c515230ceba2109e879cebed0883fb00ea2c65355759d7c6c75f60fd28f2`  
		Last Modified: Wed, 22 Apr 2026 08:24:04 GMT  
		Size: 133.0 MB (132997390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:482801a23af4453179b231faabf11d83eb249e49fa01853b27474b217c3213d5`  
		Last Modified: Wed, 22 Apr 2026 08:28:20 GMT  
		Size: 91.0 MB (90986453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f53b8243c646e0bcd1c5f6a7960855b4b7d201babdac7b844e1b7905cdec883`  
		Last Modified: Wed, 22 Apr 2026 08:28:18 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:96e14ff8e491763989f5a8fd6162b69f43222f5a16434718d99ebc50ca906bd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7508901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d57e6498671bbabbaefa9fba1ed8ca23310b3bdf21f5763789962fa21ac39b8e`

```dockerfile
```

-	Layers:
	-	`sha256:be1d346183221c265b9e54b9a86fcc79b86db7ebf69a8887ffb6756eccbca3be`  
		Last Modified: Wed, 22 Apr 2026 08:28:18 GMT  
		Size: 7.5 MB (7494668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a626df185e36c0af2fd388cef045a1247cdaf3951ffd68c8f3c50b03e0d4e00e`  
		Last Modified: Wed, 22 Apr 2026 08:28:18 GMT  
		Size: 14.2 KB (14233 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:86612c51c98329904fbef176f2c9e44cc614a4c9a28c9b8cbf6f4a84f09d6882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.6 MB (262570511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db681be2ebd1bfa30b89e86a98385a1d1cba06f12c46dcfe83ac8fc7f2b3c036`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Wed, 29 Apr 2026 23:13:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Apr 2026 23:13:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Apr 2026 23:13:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Apr 2026 23:13:53 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 29 Apr 2026 23:13:53 GMT
WORKDIR /tmp
# Wed, 29 Apr 2026 23:15:41 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 29 Apr 2026 23:15:41 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Apr 2026 23:15:41 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:943402c24d6e7299016c00f751297dfb5fc1821547fdd1d9c56a206079784185`  
		Last Modified: Wed, 22 Apr 2026 00:17:09 GMT  
		Size: 49.4 MB (49372106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a3e96a498eedeba06f7eeeef03757ec4a5de489cdb2735c62011540f27ec753`  
		Last Modified: Wed, 29 Apr 2026 23:14:39 GMT  
		Size: 126.7 MB (126652714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b51d6ae365e0a5c9301fc1af27f6bea5a82ee27d4d256a49b1e9ef6985daed`  
		Last Modified: Wed, 29 Apr 2026 23:16:07 GMT  
		Size: 86.5 MB (86545048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a977154dba30fd808d8f4e3bb04cbd4d40dd1e3be6c9f63cbc3a59cd6ea8766`  
		Last Modified: Wed, 29 Apr 2026 23:16:06 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:1279426cc1bd9eb33cf7175ffe948020cc0d12457c57af8627c916fb61ebbb9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7500975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbe6efd1e1b3c623d6767d16e57fa562efbd6cb9398ed25bf225161c508bcdae`

```dockerfile
```

-	Layers:
	-	`sha256:95035b2d9535fb282de7191ff7475729895a260fbc290c67ac314f92cad9ec5d`  
		Last Modified: Wed, 29 Apr 2026 23:16:06 GMT  
		Size: 7.5 MB (7486790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:226aba9181fcd37b444a918060fb5a6ad6cad7570372089d4acfa768093ac00c`  
		Last Modified: Wed, 29 Apr 2026 23:16:06 GMT  
		Size: 14.2 KB (14185 bytes)  
		MIME: application/vnd.in-toto+json
