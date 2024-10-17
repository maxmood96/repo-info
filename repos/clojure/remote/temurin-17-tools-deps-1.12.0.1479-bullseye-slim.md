## `clojure:temurin-17-tools-deps-1.12.0.1479-bullseye-slim`

```console
$ docker pull clojure@sha256:b7da7457e44fe991f503458459e66574ed65301a4072274a800fea0ce965593b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.0.1479-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:12a9bcd2f1f9b0473b5091d506a6866bdeb46dc14b65b59f081ee21a0ac78906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.5 MB (235536414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:247fe04b5027460d495719b9f931d08a3cc85d0b211c3321e15f736287c28aa2`
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
	-	`sha256:135a81e97634dc2d89c1ccdfc4a0ad6c6dd1306359648db263cd12e35f970cc0`  
		Last Modified: Thu, 17 Oct 2024 01:13:32 GMT  
		Size: 145.2 MB (145166561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63389ee42b198f96693d9c9837c60b1010c33921fc6a4de077241bd93e97b989`  
		Last Modified: Thu, 17 Oct 2024 01:13:31 GMT  
		Size: 58.9 MB (58940014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:799e28aa1f5c542fb8b1f77fc06782f3044bab3cc648fc22c216c3f38f9d7846`  
		Last Modified: Thu, 17 Oct 2024 01:13:30 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07af0657cffefdcb168074a08b1de55b56f01f6859fc4d4d4fae08f3ad8121be`  
		Last Modified: Thu, 17 Oct 2024 01:13:30 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1479-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:dd81d0b481e78fc81d283f40a3c0460d20a22ad73253f0173dbe9b81ac066a4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5114486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0defcbb581a506fb1ba73777a0575209b5321cbae7fffe481b4a52d9d05876ee`

```dockerfile
```

-	Layers:
	-	`sha256:f7a8b0fce146017d72f05458362920f0386963adf5e0015448a97e5a35a2d1dc`  
		Last Modified: Thu, 17 Oct 2024 01:13:30 GMT  
		Size: 5.1 MB (5098935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afc51ca8405db4763c89b0748fd0a7e16fa472e795a3d7cd7e11b77b04348700`  
		Last Modified: Thu, 17 Oct 2024 01:13:30 GMT  
		Size: 15.6 KB (15551 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.0.1479-bullseye-slim` - linux; arm64 variant v8

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

### `clojure:temurin-17-tools-deps-1.12.0.1479-bullseye-slim` - unknown; unknown

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
