## `clojure:temurin-23-bookworm-slim`

```console
$ docker pull clojure@sha256:8b7e5d4dce2dc0452a62ed5ffdf360c2d2fa803ff9e45b79497e030f70a2d113
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-bookworm-slim` - linux; amd64

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
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68fbc9263a119bec2fc9ac26afccd66ad4c297f3b4673f137ffda56f500d3f8a`  
		Last Modified: Tue, 14 Jan 2025 02:45:25 GMT  
		Size: 165.3 MB (165295089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
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

### `clojure:temurin-23-bookworm-slim` - unknown; unknown

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

### `clojure:temurin-23-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9ccf12e117dfb53720d5f45c36fbf8ccb18b7c31386707ad66b80063c23ba2bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.5 MB (260511894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a5e5e7783f4b58d557a2e0904015e0e7051ba82a7bd0b08164d4411c69f63d0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
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
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 24 Dec 2024 21:34:20 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d4c4c203eceaf699ce525e3db746048b62a1f564a7148b657207ece916a964`  
		Last Modified: Wed, 25 Dec 2024 07:38:01 GMT  
		Size: 163.3 MB (163281786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0342c3e6e2ea37b71da8315da6f9b8465b02d65765b2c3ba422afb284619a73`  
		Last Modified: Tue, 07 Jan 2025 03:36:59 GMT  
		Size: 69.2 MB (69170343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a965a85c9f52d00ff0c6146fc3919dffacb9b953f82d80a0013f1d63ba84b22d`  
		Last Modified: Tue, 07 Jan 2025 03:36:57 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:715a44b02aab040889fdaf1efb5247fc3b71c8b10911264dc4288c769eecc070`  
		Last Modified: Tue, 07 Jan 2025 03:36:57 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7192ec635a5269ed71653e05941382c009afe318df26e5c782747d5ed9d77366
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4938710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df6eb999206cf11694c8ef1ca8b34dd4016c761a8bc03c4a5ba47b904d4bc630`

```dockerfile
```

-	Layers:
	-	`sha256:db1382a473888755da6c14fd97a177bee82e92d2fd920b8a375a5d53bd49b6a5`  
		Last Modified: Tue, 07 Jan 2025 03:36:58 GMT  
		Size: 4.9 MB (4922714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49a9beb78cee005265c44cc61d39390c5f172508b1bbf7288c4d541cd5958170`  
		Last Modified: Tue, 07 Jan 2025 03:36:57 GMT  
		Size: 16.0 KB (15996 bytes)  
		MIME: application/vnd.in-toto+json
