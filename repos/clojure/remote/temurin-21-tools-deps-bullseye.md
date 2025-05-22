## `clojure:temurin-21-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:967e7b8c8b7d8b8de0ea7499d86ca73448f878fd5347eb382bc0b3dd756a9111
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:1d20fc84992f54f3135a0b670290277053e08374fb3acd37de4ad6c9533b14a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.8 MB (280784416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9126c20feeecd3afa0065ee7452ffde3470f093a1bc65aae929afd13d8706cd6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:54107f2de180b7b6e9f909d2f1c6c18e10c700a6bd80a035d931768b06bb2905`  
		Last Modified: Wed, 21 May 2025 22:27:58 GMT  
		Size: 53.8 MB (53750195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a890068bf1806a44acb308eed42fc802e900a56e5a5bc157868bf13c7f5a5e53`  
		Last Modified: Wed, 21 May 2025 23:33:33 GMT  
		Size: 157.6 MB (157634458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f185aea90b4822509ce949fc98c9f06f36d2fcfca2f0efe1db7d2bc3303693f8`  
		Last Modified: Wed, 21 May 2025 23:33:32 GMT  
		Size: 69.4 MB (69398723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b2c0ec17e508f66362e297803c79d3a52af458ee7e98585cc39507da5da382`  
		Last Modified: Wed, 21 May 2025 23:33:31 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6c9175cef5584b4dcf17a368db66d17324bf0895a25d1fa519540fd9bb243c5`  
		Last Modified: Wed, 21 May 2025 23:33:31 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:21e403932ab647c5a2e3d79b77707a92653079c620f8ab741e242ebd71fca52f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7274865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d76bc69073af1cece2a36cbf5b467f110253305b55ad4d046cc7634e6eb91e8`

```dockerfile
```

-	Layers:
	-	`sha256:64181c04152334dd81f5f39d05cf7d543b6fcf3f2b530a68568243b74fbf5c86`  
		Last Modified: Wed, 21 May 2025 23:33:31 GMT  
		Size: 7.3 MB (7258368 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfe750d9b7d6cc8069968339dbf0ea6fde1e0364cfee4949ef055474e747b113`  
		Last Modified: Wed, 21 May 2025 23:33:31 GMT  
		Size: 16.5 KB (16497 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ce72cf9340f0355dab310428b1b4ebee37cc88593da095105369f8391299f0e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.7 MB (277705241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb5e1d52e4983669ec5b04351b73d93d59c727fbabd70e1e0a8804da9d4904f3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1745798400'
# Mon, 28 Apr 2025 17:24:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Apr 2025 17:24:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 17:24:54 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Mon, 28 Apr 2025 17:24:54 GMT
WORKDIR /tmp
# Mon, 28 Apr 2025 17:24:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 28 Apr 2025 17:24:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9ce0153b823c3af508e9c8a003aa35daca140e8f4578ff2a451ac20469ea739a`  
		Last Modified: Mon, 28 Apr 2025 21:20:53 GMT  
		Size: 52.2 MB (52245979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61c157ab8eb81c07fbfae63cd9fe879f3c276295291ce0524b491f7a359eb662`  
		Last Modified: Wed, 30 Apr 2025 01:46:35 GMT  
		Size: 155.9 MB (155928834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13506fe2d6b2ce347edd3ab615a7bd796a465f1e3d60da021f0acf8f602c673e`  
		Last Modified: Wed, 30 Apr 2025 01:46:33 GMT  
		Size: 69.5 MB (69529389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea4e74d14199dd011282c596a864ad8576b2f9edb40fb804e97b1a5d6e58118a`  
		Last Modified: Wed, 30 Apr 2025 01:46:31 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0678d31f455b7f7b6bd02121b70371c5a7d3b38fc718a04f40c3d2b9584139e3`  
		Last Modified: Wed, 30 Apr 2025 01:46:31 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:1eed434ff00f0f2eda245eb11912fac6bbeeee264952df0b6aac49e61394d117
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7232095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efd9cd84751c76ba00efcff59c351fd368383c3a879d0d077a4a938183b67da1`

```dockerfile
```

-	Layers:
	-	`sha256:5468e2840553d639dc66aaecf4f1d0c6c7499bce073205ddad0f43f73a2db679`  
		Last Modified: Tue, 06 May 2025 00:44:40 GMT  
		Size: 7.2 MB (7215456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7babed322b71735677b52d9a38d67d6d2f00a11fa5d26242293716ab77d4c803`  
		Last Modified: Tue, 06 May 2025 00:44:40 GMT  
		Size: 16.6 KB (16639 bytes)  
		MIME: application/vnd.in-toto+json
