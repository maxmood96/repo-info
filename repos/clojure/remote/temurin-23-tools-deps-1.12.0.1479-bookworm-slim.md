## `clojure:temurin-23-tools-deps-1.12.0.1479-bookworm-slim`

```console
$ docker pull clojure@sha256:eade0b86e6c72d5f1e44084a6d769c6d55ce320265e70342b80eae40822be542
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-tools-deps-1.12.0.1479-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:643006e20b8c056e6460c6fca6855bc0a3345f8569c8f8dd2781bcd3b1d3f000
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.8 MB (262820336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f107f88ad37cec8e783483b619967ffbaf3b48c376cf390032c877abcb7d8973`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2403e384111eb93c9561c8f5a6c45cb953d6ab74b744c597efa514734e295db`  
		Last Modified: Tue, 24 Dec 2024 22:38:51 GMT  
		Size: 165.3 MB (165295091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79e2c8f9a3496a1a37c6c9bfc62055dc959508c178cf5111d1949abcf84d5985`  
		Last Modified: Tue, 24 Dec 2024 22:38:50 GMT  
		Size: 69.3 MB (69292627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7852d43dc72a2a0732d1eb349288bdf7a2128d86ace40c3fe0b9399ee496a27a`  
		Last Modified: Tue, 24 Dec 2024 22:38:49 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7caff11ddd18b1dcb776b73f31d944062ac7ed32f86f08eef7c19f0bf08398f8`  
		Last Modified: Tue, 24 Dec 2024 22:38:49 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-1.12.0.1479-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:45e106e3db631c12c3b107274418f934221a9079be7d59070f0ee1938ae9d607
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4933390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98a246aba1aeccf91d76557b9247baf47a9386ac352ad252c6c93129633799d9`

```dockerfile
```

-	Layers:
	-	`sha256:c27111a8678f155e4bf84255b6f1b6677418a9b748accda86342075ec1d452cf`  
		Last Modified: Tue, 24 Dec 2024 22:38:49 GMT  
		Size: 4.9 MB (4917512 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35abc21cb631a2bc198025ac619cd9c2613881123c493033cacd16dd16c51835`  
		Last Modified: Tue, 24 Dec 2024 22:38:49 GMT  
		Size: 15.9 KB (15878 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-tools-deps-1.12.0.1479-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:15152218d1f23aab4d94c665628722af9376159fad1317325e2047db30b87705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.5 MB (260482805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c771fee9ff77d6d2ea469ec39edc49dbcf14e31d89b0dbb66c72d0e3aca18430`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
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
	-	`sha256:75e279628577d9c3f0dd99c12991e7024fd2579db844c899b74a8012a1473701`  
		Last Modified: Wed, 25 Dec 2024 07:41:24 GMT  
		Size: 69.1 MB (69141260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc36bad098a4bc4538e0ce7e6c6f4e34afed9a69c930a5fa7b5e5fef4446fd52`  
		Last Modified: Wed, 25 Dec 2024 07:41:21 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f2d23041050503493b61fc1ed825aa9046d48890ec8e486090eed256acc0fdf`  
		Last Modified: Wed, 25 Dec 2024 07:41:21 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-1.12.0.1479-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:09e2740b195df0581b2550a2ddae2456a2ca0556527172409b2bf6d64bf8baa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4938648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e195cc0174b237db604b4bb426dd9357539862faf9d10a6e93cd47ec21e13742`

```dockerfile
```

-	Layers:
	-	`sha256:cf1d6e8518a38e86964b4496a3cb9ba912963612b4a45a548c571cd232f35c0b`  
		Last Modified: Wed, 25 Dec 2024 07:41:22 GMT  
		Size: 4.9 MB (4922652 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:736f87a582298c1392bc1397547fa0cbf168b5a4e660a9b6f4a023d1c800aa51`  
		Last Modified: Wed, 25 Dec 2024 07:41:21 GMT  
		Size: 16.0 KB (15996 bytes)  
		MIME: application/vnd.in-toto+json
