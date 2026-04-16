## `clojure:temurin-11-tools-deps-1.12.4.1618-bullseye`

```console
$ docker pull clojure@sha256:d7e564ed424d4bcd879bac4801dfb2486c92e140de1ccca6634f87a7ed9da309
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.4.1618-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:819fd813d576e3dd5c40dc267daac9a7a9109cfdb5469922ca7b0cb64fea5a62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.2 MB (269171097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43631693e79437eb1fc8647059da6749af0dec2ed30f43b390623cc842fad8eb`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Wed, 15 Apr 2026 22:03:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:03:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:03:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:03:03 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:03:03 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:03:17 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:03:17 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:03:17 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ced3088fc7691915325d6187786ba346149f7c9dcdbfb3772ca71be74bf87622`  
		Last Modified: Tue, 07 Apr 2026 00:10:43 GMT  
		Size: 53.8 MB (53762793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:694a66ecbc5c5c6013c126f5d3310ca21ddab21b654c846199da52cca5a562dc`  
		Last Modified: Wed, 15 Apr 2026 22:03:42 GMT  
		Size: 145.8 MB (145806800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c725499eb0cfc8944024b0313faebcddc6413f0ca865a97fe499d2d74ce6cd75`  
		Last Modified: Wed, 15 Apr 2026 22:03:39 GMT  
		Size: 69.6 MB (69600858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56e96027c648326f4aab65c567373ec9ca4425f3e547f1b5b7482090b58bfead`  
		Last Modified: Wed, 15 Apr 2026 22:03:36 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1618-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:cc407f23460363af32df44553189934d8b3701d05f1f7eca8c4f69a952b44b0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7442003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c711b634093e4fa631c8196b43ea23185421c530ea532e3e4dbedaead3ff9ce6`

```dockerfile
```

-	Layers:
	-	`sha256:eb56fa26e2079466b964f044debd8635bf765d9c22ee42055fe89c580f297baa`  
		Last Modified: Wed, 15 Apr 2026 22:03:36 GMT  
		Size: 7.4 MB (7427794 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8eeb904fce4f574f3b89956889abf2e9096d6ad7def16a225b63f044754c4818`  
		Last Modified: Wed, 15 Apr 2026 22:03:36 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1618-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6cd9f91912c95f2718d64f348415841b0ea939fac2837d06d3c11eaa7967104f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.5 MB (264485241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4820452c7df9d04aa4dbbe672e30038b764971d2b9734f380e86d2766a506b94`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1775433600'
# Wed, 15 Apr 2026 22:13:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:13:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:13:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:13:30 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:13:30 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:14:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:14:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:14:26 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:910d955c4ed64a8ee0854ded27fe508086448dca2dcf21a0af023b8bc9d2020f`  
		Last Modified: Tue, 07 Apr 2026 00:10:48 GMT  
		Size: 52.2 MB (52247615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca110c84f751b3f67a74459d3952144bf4b419f2d11cd8d620f4df8bfbf8611`  
		Last Modified: Wed, 15 Apr 2026 22:14:06 GMT  
		Size: 142.5 MB (142500804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:834bb736518cced4e553f6307dd56311f26fb53fbdd3d73cb8eaff2e186ef64f`  
		Last Modified: Wed, 15 Apr 2026 22:14:45 GMT  
		Size: 69.7 MB (69736176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71fb867aa7495cb3cfc1103bb0e5095aa8808ec86683ca3b9a42e1c03b20bdfb`  
		Last Modified: Wed, 15 Apr 2026 22:14:43 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1618-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:63cf8978bada19ed79875b5c20f35432b6ff2605327841992d9cd3e03f7782eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7447837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ede6e92e5ff4750a8d7aafa9e0fb11b3064a8b7239a9ad3f81bae149d0791189`

```dockerfile
```

-	Layers:
	-	`sha256:f0356bd5f87f1a747da02321daeaeebad3060d57de3eb4c501a7ba16c3fe244b`  
		Last Modified: Wed, 15 Apr 2026 22:14:43 GMT  
		Size: 7.4 MB (7433511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3c979eeb4e144358fb99d183a16fb26146f2cbf946b0d00683d99e0dafbfe1d`  
		Last Modified: Wed, 15 Apr 2026 22:14:43 GMT  
		Size: 14.3 KB (14326 bytes)  
		MIME: application/vnd.in-toto+json
