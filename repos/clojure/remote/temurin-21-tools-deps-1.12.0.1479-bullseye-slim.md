## `clojure:temurin-21-tools-deps-1.12.0.1479-bullseye-slim`

```console
$ docker pull clojure@sha256:656311869e9217b63d645995200d45f33fe3f9b60db3aab5faf1607f878f140a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-1.12.0.1479-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:d92b4711af0dd90eb26655722362795b066b476dd71cc759e8ed49119ec60692
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.6 MB (246578452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2486127f68bca8e2b7ef333797376ad4d0151b8ea1b2c8976c54aadb7190962e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
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
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fa1805c88fab089f4a11f055d0117232de7b7a3dbaaa6643c5367734a6b6011`  
		Last Modified: Tue, 03 Dec 2024 03:25:51 GMT  
		Size: 157.6 MB (157568673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef6576be0474378ecc84e5189b8d9024c54ca7156273ee08a00edb55a6e8d15f`  
		Last Modified: Tue, 03 Dec 2024 03:25:50 GMT  
		Size: 58.8 MB (58756100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fad9a7c4b3ea6c8cf650b9e5ecc428d17a181894a098567494ebbfe5b6fd4f2`  
		Last Modified: Tue, 03 Dec 2024 03:25:49 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44886777db8be53659781a1f3e8874734adc0730884ff4c0196ff68022a49323`  
		Last Modified: Tue, 03 Dec 2024 03:25:49 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.0.1479-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f6237803d26fa4a5d28d4369c8ad42786be7c7973d4aed7ea776d597d5f9fc6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5143927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7bd3472bb9c3be6473dc81b1aca2800edd71544380e28f654114ab33b5d4a8e`

```dockerfile
```

-	Layers:
	-	`sha256:9461e54a2b3cf62754e0c892df04a5c5db6bd33b8187123490260a0fc1d12984`  
		Last Modified: Tue, 03 Dec 2024 03:25:49 GMT  
		Size: 5.1 MB (5127352 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65ac9036a11194519edbdbceb173166b6e8007a84b58e10a3a660f659badbb16`  
		Last Modified: Tue, 03 Dec 2024 03:25:49 GMT  
		Size: 16.6 KB (16575 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.0.1479-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:dc9b286ed9d6f41d2bcb232ca5e1d0f6426e8ca53c4664ccc0a31e363e1e5e8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.4 MB (243419315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63c3d34180791caaa926519f3528467293a8c39eba2581bca75dab9b976ffe6b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
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
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef51106499142bb6c90e581ecf9486920ddcb10cbaf0fc6e963d21ca014f68f`  
		Last Modified: Tue, 03 Dec 2024 15:26:53 GMT  
		Size: 155.8 MB (155793104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa04d85d3ddc4da6ae9c9d0353924e88c7af0d82184f8caef20ed270ba4ff6d`  
		Last Modified: Tue, 03 Dec 2024 15:30:29 GMT  
		Size: 58.9 MB (58880247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8691d973eb66be62e9e4b6a678a3419733c293c1d83d35533980167be4fa3e0f`  
		Last Modified: Tue, 03 Dec 2024 15:30:27 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e895502ecdb0f2b832b8614150b599ed4eab267cb170651424adca775a61835`  
		Last Modified: Tue, 03 Dec 2024 15:30:27 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.0.1479-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2ab3fd9934f5b6430c9c8ecee85e403acf2600b8c385d5e41cebf153683e9037
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5149830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4462f2139ddd19106c946304e1bbedfbbd7351cdd32b6556f207b4794c1d3e88`

```dockerfile
```

-	Layers:
	-	`sha256:9cf496fb8bf0755b8035c154b178dc60cdbd3aa1ec1b2a92ce049cb8af9bbde2`  
		Last Modified: Tue, 03 Dec 2024 15:30:27 GMT  
		Size: 5.1 MB (5133113 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba145b1ae81d9ccc40ed336119a4a77944b0c4953b6cdb0f04df452ed3ae2826`  
		Last Modified: Tue, 03 Dec 2024 15:30:27 GMT  
		Size: 16.7 KB (16717 bytes)  
		MIME: application/vnd.in-toto+json
