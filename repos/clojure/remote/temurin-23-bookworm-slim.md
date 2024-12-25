## `clojure:temurin-23-bookworm-slim`

```console
$ docker pull clojure@sha256:f363afb8ce9844469f9e87711a0debc0724b4d2d821cb74a7d1af334b5d37904
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-bookworm-slim` - linux; amd64

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

### `clojure:temurin-23-bookworm-slim` - unknown; unknown

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

### `clojure:temurin-23-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:acc7c3f36382ac12c0ce0498a72d245e35666a64f7486ab4ea21c50f872f5bcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.5 MB (260482715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:771b0501c22b9ed9187ecc2ddb0e5373635f0472e7a340d0accde5facd8b4d11`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
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
	-	`sha256:bb3f2b52e6af242cee1bc6c19ce79e05544f8a1d13f5a6c1e828d98d2dbdc94e`  
		Last Modified: Tue, 03 Dec 2024 01:30:11 GMT  
		Size: 28.1 MB (28058810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3982780e928391e952f0145329b70cf65022247473d929b5421291c274f82ef8`  
		Last Modified: Tue, 03 Dec 2024 15:33:09 GMT  
		Size: 163.3 MB (163281795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a88f5ac7f037f635af83b79502093754de00b45ebdb115ea3f415608d5aee67`  
		Last Modified: Tue, 03 Dec 2024 15:37:24 GMT  
		Size: 69.1 MB (69141068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc9dad40b02f0e75835dfc4089b5816c137b97d5ecd9d7c775557a05d06bce86`  
		Last Modified: Tue, 03 Dec 2024 15:37:22 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98fc329d98a0d9c16ae728466a0401ed9a0ead5cf78062f97bd098dea7545da`  
		Last Modified: Tue, 03 Dec 2024 15:37:22 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ef7abbab89fafe5a52a2bd9741b0ee103f3984f30c4b50ccc826804c175745fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4945532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fa6b53f8caedeb2e9dfef31327c5f2c0760b3991c0b2ffece4f87064d6f987a`

```dockerfile
```

-	Layers:
	-	`sha256:68f86399b37474f9ed327dd881454719beab40ffe36437c16d4789aab43de138`  
		Last Modified: Tue, 03 Dec 2024 15:37:23 GMT  
		Size: 4.9 MB (4929537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44b437ebe2e51709a57cd09200cf2cf28dd61e79c9d2a7fd24530bea4fe3849a`  
		Last Modified: Tue, 03 Dec 2024 15:37:22 GMT  
		Size: 16.0 KB (15995 bytes)  
		MIME: application/vnd.in-toto+json
