## `clojure:temurin-17-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:42ec58853762b166a8ecf3ac4db6a68984fa56e19eca13d7fe8f234ef4cce5f8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:4e1a5d012f7aa65e29cd2bd0aa223ff299f61d1d5de355dfea749ff1c1e28780
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.5 MB (235536441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1c8e1b522ee68c8ac5c48ab3648c0654328f616b6332bedbe79c6b2d5a3d0e2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:0f6f1b93a8fddd20b36a99cc6cfbe4a03bc7be2adb427f7f8e74a2029c54c8bb in / 
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
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
	-	`sha256:6dce3b49cfe6dc4b4e0198412bb0578215c86dae41303c47438639853bcba562`  
		Last Modified: Thu, 17 Oct 2024 00:24:36 GMT  
		Size: 31.4 MB (31428800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7ad995427cdea099cfee6bb165741e1e35b437f97959525b6b939b6a4ae4df5`  
		Last Modified: Sat, 19 Oct 2024 02:59:07 GMT  
		Size: 145.2 MB (145166530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e433b7105f5df4859cccecaae8d4bbfe332690e2fbc578dea849b8849529ab2`  
		Last Modified: Sat, 19 Oct 2024 02:59:05 GMT  
		Size: 58.9 MB (58940072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59243820d5753c264d1351f781518ca9ac3ec500180ffe8d3488cdbd8cb6a5c1`  
		Last Modified: Sat, 19 Oct 2024 02:59:04 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e96e63ff3e5fe31131da86340ff37583dbd0f50efa0852dc30c2737f6ce60d`  
		Last Modified: Sat, 19 Oct 2024 02:59:04 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a70913f10c50779913945855efb61135543517220bc46cd89c8927e57b834c53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5140399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9aed94e246e3d07abdd711cd0b279b70b60cde9cafc7b789634383c33e03b3f`

```dockerfile
```

-	Layers:
	-	`sha256:cdff3dd8552a2d1c33b250f74f583ab1e2a3563c49f9da80c6a36f91ba50c829`  
		Last Modified: Sat, 19 Oct 2024 02:59:04 GMT  
		Size: 5.1 MB (5124680 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c48d4f9942ce50bf8a4a399cc174d30d594161a66ead944cc08621bd47721bed`  
		Last Modified: Sat, 19 Oct 2024 02:59:04 GMT  
		Size: 15.7 KB (15719 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d8ad99c5a31c8e44be45a4ef13b00311fa843b0cb0d31c2c7730d1db70ede307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.1 MB (233109594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16d787a7361d3f3fd75452f50df9867b8b987544bbf788354f562ac95a1f8ab0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:f3f9a52e18a8da911b50ebddcc922d4b5a7aa8caa6eb15fb5c26c696b8fe9610 in / 
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
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
	-	`sha256:b3c56a24ca3234ee90349473402ac1b368a2fb3c9620242fa70a85d7396d7799`  
		Last Modified: Thu, 17 Oct 2024 01:15:14 GMT  
		Size: 30.1 MB (30075757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:414bb17c66e1a956e8e8cfbcd993934c289b1940da79f19f4baaede4b6a72b09`  
		Last Modified: Thu, 17 Oct 2024 08:15:01 GMT  
		Size: 144.0 MB (143959469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e843b20dcbbcb8d26f7e23db89798c53bdfccf4af1db5665bbda7f438f530e`  
		Last Modified: Thu, 17 Oct 2024 08:18:35 GMT  
		Size: 59.1 MB (59073327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ce0c9c7f61f754523bcb3ce63bc47bac67e808339c35c6c267d49436d72904e`  
		Last Modified: Thu, 17 Oct 2024 08:18:33 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd3c96beb6d25f59136439d6a321a0a1a76e2c4e10bff405aa05a1d0c037eb22`  
		Last Modified: Thu, 17 Oct 2024 08:18:33 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3acd074119c7253df3d35e67ed24e41a363f6d9a34ad0a49268cafe9b64c8cce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5120328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc0e32410969b82971f71845a60303ce0f5cfda098f443d5b6d45850531f0597`

```dockerfile
```

-	Layers:
	-	`sha256:af02ef773caf3edc2a1f586b3dea648f53b4d84780888b6bc64b7f4392db399e`  
		Last Modified: Thu, 17 Oct 2024 08:18:34 GMT  
		Size: 5.1 MB (5104672 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7372095ed70985f524d3618e65979ecc63edb16b8193aa0f2aea7c0fd28d07a`  
		Last Modified: Thu, 17 Oct 2024 08:18:33 GMT  
		Size: 15.7 KB (15656 bytes)  
		MIME: application/vnd.in-toto+json
