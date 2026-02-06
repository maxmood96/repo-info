## `clojure:temurin-17-bullseye`

```console
$ docker pull clojure@sha256:56d917eff94fdf996e3f0ea42b5bd3c232dc4d9c5fd27b11a266053bf8a1f152
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:d4d47d3561c80db20c2de32341251d17b01f41d4364b58f0d2039b6c7ab55397
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.9 MB (268927444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0649f213108575678c090a203290fa47f11dd2a9d461c23604650468868ac786`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Thu, 05 Feb 2026 23:04:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:04:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:04:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:04:45 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 23:04:45 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:04:59 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Feb 2026 23:04:59 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Feb 2026 23:04:59 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Feb 2026 23:04:59 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Feb 2026 23:04:59 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4837b8a287e31893a57c67e4e7e49ea3681edb8424480549d8b5f5b29691313e`  
		Last Modified: Tue, 03 Feb 2026 01:13:50 GMT  
		Size: 53.8 MB (53756259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b32de76c33f3f79b8c3ec4aa80fc16e5459e241d479bddd2582e648e2a2025a`  
		Last Modified: Thu, 05 Feb 2026 23:05:22 GMT  
		Size: 145.6 MB (145628484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5d493a7057beb984940fac92fecdcadabd1f6243922f5721e64731e99d8c01`  
		Last Modified: Thu, 05 Feb 2026 23:05:20 GMT  
		Size: 69.5 MB (69541659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea407e8f1b5528803a567a41800e50fff3be20d01bdb6315dfe64633badff74b`  
		Last Modified: Thu, 05 Feb 2026 23:05:17 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd7cdfab0c951e6a714827628fb3e29d88b9bff50cf510922e4df0b332492def`  
		Last Modified: Thu, 05 Feb 2026 23:05:17 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:d97df7c9b3797a802a9326aa1c345a34d27ca2a10177c44ebd4d6a9012011c59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7413498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c4de51d40d7de182cae1b4526e1b59f4a35dfb7f5b3ec725fc49ee785411598`

```dockerfile
```

-	Layers:
	-	`sha256:8093126f7d86688e1b53a891f44eb7ae18d139cce80dc180163c264cef2b1381`  
		Last Modified: Thu, 05 Feb 2026 23:05:17 GMT  
		Size: 7.4 MB (7397720 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c53d88bb9bf19c2c966c66c5cc233a10a3a94614d8668a795d9bf9df976e77a7`  
		Last Modified: Thu, 05 Feb 2026 23:05:17 GMT  
		Size: 15.8 KB (15778 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c7f68e90c1b3e47f085c266d299552ac0640692ee5580cab1839898daadfa9ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266389035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d8893ca0f9dc821d2509bf003a7f239c0fdd9a177768843f75ae102ecd0ad46`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1769990400'
# Thu, 05 Feb 2026 23:05:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:05:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:05:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:05:37 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 23:05:37 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:05:51 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Feb 2026 23:05:51 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Feb 2026 23:05:51 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Feb 2026 23:05:51 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Feb 2026 23:05:51 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0742c20cdb1eb0c212cefb0ff441553e29e6ccfa92b808cca3d7e8548a6fd569`  
		Last Modified: Tue, 03 Feb 2026 01:13:54 GMT  
		Size: 52.3 MB (52258320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afebc81b12f3ebbb343b10f8752a9e890bba9838ceff5cac18effb868a44227b`  
		Last Modified: Thu, 05 Feb 2026 23:06:15 GMT  
		Size: 144.4 MB (144436240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05ebb6b75d11f65034322fa694be0e8919d0f097e8e0f24e58147a3bc17f271`  
		Last Modified: Thu, 05 Feb 2026 23:06:13 GMT  
		Size: 69.7 MB (69693431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79c392a87b6c00ec2add3238cb50648351932a7f8bcdf0b27c00ae4601dac355`  
		Last Modified: Thu, 05 Feb 2026 23:06:10 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f945ff0c6f616c710e00332dae15554b2a84d296f7af3966ed4af89cf6ff0b4e`  
		Last Modified: Thu, 05 Feb 2026 23:06:10 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:0445dc2b041450b875a4cd3d03976a7d19d6e9c6a9df4959566a765a71038dfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7418715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4589ecd6dde41124ad6f2317a99623036b330c5d599b224ef1b6cf1fa2526601`

```dockerfile
```

-	Layers:
	-	`sha256:5c48e8f8af02d56f3dc129433bd6967c385710861629668a49b9d9ea24e1c955`  
		Last Modified: Thu, 05 Feb 2026 23:06:10 GMT  
		Size: 7.4 MB (7402819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30732bc684dc58e01ba2cb5bd38471c05d2828aa1089bb1c4c7adb7dc1e2572f`  
		Last Modified: Thu, 05 Feb 2026 23:06:10 GMT  
		Size: 15.9 KB (15896 bytes)  
		MIME: application/vnd.in-toto+json
