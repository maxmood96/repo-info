## `clojure:temurin-23-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:1b673cc0411b52d129f75b6abfebca2047fd6d501f5c2aeb5b9693029fb3edc4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:0309f4b9a42643d676b724ede134a9969c8d9a571cf9823150a14429e652962c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.0 MB (263034473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5817a4778fe686fd0ab8dc19a5f11ff47ca7c34f89476469cb03f914feaee8f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Jan 2025 23:07:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:07:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:07:46 GMT
ENV CLOJURE_VERSION=1.12.0.1495
# Mon, 06 Jan 2025 23:07:46 GMT
WORKDIR /tmp
# Mon, 06 Jan 2025 23:07:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8408034c095c531155acb08bef65ad1edf25f55226bb086dfaf0d0eee9cadd59 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 20:32:59 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68fbc9263a119bec2fc9ac26afccd66ad4c297f3b4673f137ffda56f500d3f8a`  
		Last Modified: Tue, 14 Jan 2025 02:45:25 GMT  
		Size: 165.3 MB (165295089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46f8622d4c37a4631809ddb6ccf332192e5d0fb9e2535e612384dedb796fa5ed`  
		Last Modified: Tue, 14 Jan 2025 02:45:23 GMT  
		Size: 69.5 MB (69525927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a012237713dc6ac233360c36dbf5267be2ab9741b974f5487e29f84a0d0e0b4`  
		Last Modified: Tue, 14 Jan 2025 02:45:22 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fcc0054495be97ae61588879b0b52d73a49b5769c45adcfac3fa5a38528bcf3`  
		Last Modified: Tue, 14 Jan 2025 02:45:22 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7c4bd36f2efb5c6198f8202f65df2e86cf97feed1804ce452eb9683e814a1a2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4933451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:141b69396f8a10203ed9024367088a97d1510d617914d14431ecb3ee43918309`

```dockerfile
```

-	Layers:
	-	`sha256:bfc3bdf2a889126bf6c39b7640d608c554429c7f9997b55e3300836e3ede2b0e`  
		Last Modified: Tue, 14 Jan 2025 02:45:22 GMT  
		Size: 4.9 MB (4917574 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d7da93f1642b3cb36b0b33b0cb1e19985bc4989b40e09d5daef7712bb57aa41`  
		Last Modified: Tue, 14 Jan 2025 02:45:22 GMT  
		Size: 15.9 KB (15877 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:15aa3e38d596320a8e4a404b0ea405ffe6b85a74fa1ea41821c1ab142ca16d70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.7 MB (260697757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c65b8bf7c246f27bc35c5625ad1d205ff23bc5495358cd5e99cf0cbcd781f61`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Jan 2025 23:07:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:07:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:07:46 GMT
ENV CLOJURE_VERSION=1.12.0.1495
# Mon, 06 Jan 2025 23:07:46 GMT
WORKDIR /tmp
# Mon, 06 Jan 2025 23:07:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8408034c095c531155acb08bef65ad1edf25f55226bb086dfaf0d0eee9cadd59 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:206562aa8986622145ccd160d0b201aadb283872c341606fbd554109da8e6b98`  
		Last Modified: Tue, 14 Jan 2025 12:39:56 GMT  
		Size: 163.3 MB (163281808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13312071bfda21385c0cdf28555656fb422e61fd3185e50ee075d4de0d64aa10`  
		Last Modified: Tue, 14 Jan 2025 12:43:14 GMT  
		Size: 69.4 MB (69373876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998f6f830ab5357ad0428c57a4394fca9957e7c46a796db74363514fb6ff71b4`  
		Last Modified: Tue, 14 Jan 2025 12:43:11 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17f7e1b22d465c8e0e190b715cca3ce0c29245cf0de07840e1bb714bcc955ab7`  
		Last Modified: Tue, 14 Jan 2025 12:43:11 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:be8d7ca3c9a991670ca58d9b06536f131dc3488bc2fa7f8ae93eac19919a4718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4937910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1dcb3aae95e81e3e857fc16f9570dfa5f0b50751b3a9912a8350dd6b7f422fe`

```dockerfile
```

-	Layers:
	-	`sha256:ed927dad4a2a40ab211c4c6ed4c67b5058ec82dd3f7ca93c896d391f62ca4145`  
		Last Modified: Tue, 14 Jan 2025 12:43:12 GMT  
		Size: 4.9 MB (4922714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cad1ba574b92b46a874f4b6acba4ea694633664a39d8e0f5c18610fbd45d1a8a`  
		Last Modified: Tue, 14 Jan 2025 12:43:11 GMT  
		Size: 15.2 KB (15196 bytes)  
		MIME: application/vnd.in-toto+json
