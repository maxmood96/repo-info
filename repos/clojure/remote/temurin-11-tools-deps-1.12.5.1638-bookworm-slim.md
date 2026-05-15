## `clojure:temurin-11-tools-deps-1.12.5.1638-bookworm-slim`

```console
$ docker pull clojure@sha256:8b48dcd51c49866b6b5dfc4e3d105aa4dd1beea365a98b704f3fdcaeb63641f6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.5.1638-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:f97f0d14562da6cf2fe3c4dd93726a05555f3b4b18a9f5eb89010abffbd908e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.9 MB (243853766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18842e42a06beebe9719dd01da653d7c646ae81634bc70519a61e7d36f16dedd`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Thu, 14 May 2026 23:34:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:34:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:34:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:34:24 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:34:24 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:34:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:34:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:34:39 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd9756ec11d9dc3de58e9a108610b781a1359f02cb273f42e2788749494e7062`  
		Last Modified: Thu, 14 May 2026 23:35:00 GMT  
		Size: 145.9 MB (145886263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07bc486fed49e68892897df4e7dcea3679603c1122659e784b8039fa6f4130a9`  
		Last Modified: Thu, 14 May 2026 23:34:59 GMT  
		Size: 69.7 MB (69730572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5596ae84762e87ced8ad2d21fa67d11e2a25a233806bd59acd4d1554af96239`  
		Last Modified: Thu, 14 May 2026 23:34:56 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.5.1638-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4b04e7a1441311d62b950bf1afab778d9b41a1e554c6a49a948f1531c7db5985
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5150729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de7f472efe15ced31af039bcaa0d175b5be1efb7e9ccdb114c635bce14646ede`

```dockerfile
```

-	Layers:
	-	`sha256:2e37a9ecea6d8ca75ada7a4591814a103a5c9ac832cc2beb1faf69273dec9a3a`  
		Last Modified: Thu, 14 May 2026 23:34:56 GMT  
		Size: 5.1 MB (5136308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac50fe7be16a016a88108f1270effb37479eb5afa339950036fbb1f68182a798`  
		Last Modified: Thu, 14 May 2026 23:34:56 GMT  
		Size: 14.4 KB (14421 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.5.1638-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f231dc9e474ca399c6abcc4377de19f15274c82648119ce9d9bc38216ef53ad5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.4 MB (240421394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18935bd543373bfde8861b4ff09f08fc793d214119851a07da3710aa23635acb`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Thu, 14 May 2026 23:34:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:34:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:34:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:34:18 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:34:18 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:34:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:34:32 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:34:32 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:6a2d07df495cc055bce0251fe801ee08db90750f52e43a555be5dfd8f5023783`  
		Last Modified: Fri, 08 May 2026 18:24:52 GMT  
		Size: 28.1 MB (28116165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b59a86267c73179a7da9be200ac71568032963497d97f7ffe736c8fc69dcfd5`  
		Last Modified: Thu, 14 May 2026 23:34:54 GMT  
		Size: 142.6 MB (142582228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50f7a91e93b5875bcb32bafae3d22199f78bfe7d50b831734d008acc9ca164ed`  
		Last Modified: Thu, 14 May 2026 23:34:53 GMT  
		Size: 69.7 MB (69722353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73af006dc96c3bda7106ec50c59c5b05587cb580342327b5cfb233adeedcfba4`  
		Last Modified: Thu, 14 May 2026 23:34:50 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.5.1638-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:098b4814c5155c0b0261ee5ee4268a7a4a82a90d0ad3533006dadd6d3935800a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5157226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f652d56b4d22e961d0f0aae0ecbd6eba466e31863948d0b250330d58bdc8af38`

```dockerfile
```

-	Layers:
	-	`sha256:784d82ae92144e44a522a74e6ab309e65b3fc3c47e72185c574453d859b0b149`  
		Last Modified: Thu, 14 May 2026 23:34:50 GMT  
		Size: 5.1 MB (5142687 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fcdccdf4e5b01de9bec151dad1922e5a51f6358ea963cf7054ae19df853e1c4c`  
		Last Modified: Thu, 14 May 2026 23:34:49 GMT  
		Size: 14.5 KB (14539 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.5.1638-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:62fdc14c0d87c6f80d4a627cf832e0e4decbbfcca1aee4054fb916f7b5de5000
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.8 MB (240754895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb3ef2abef41d1e9b95d7a142a783d5e2d72270a8405081cef747c043f24f858`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1777939200'
# Sat, 09 May 2026 02:25:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 09 May 2026 02:25:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 09 May 2026 02:25:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 May 2026 02:25:33 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Sat, 09 May 2026 02:25:33 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:39:00 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:39:00 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:39:00 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:0e29ea7436ed4beb1c38bcfee44589407e49fc690669b42b35db33a9588e820a`  
		Last Modified: Fri, 08 May 2026 19:44:06 GMT  
		Size: 32.1 MB (32078453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0a6cd9ce9367000978e62d727341fdbe8bd162e7346e254771317696df2b498`  
		Last Modified: Sat, 09 May 2026 02:26:34 GMT  
		Size: 133.1 MB (133110215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a500219d5bfb2ccd8c20ec1efc5f08bc5ebd94748c323b2494f6e505f016da0f`  
		Last Modified: Thu, 14 May 2026 23:39:34 GMT  
		Size: 75.6 MB (75565579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b7a2eab2ae51fe88bfdd96690bfd35b51f3b6447b2274da92ee6849d8055524`  
		Last Modified: Thu, 14 May 2026 23:39:32 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.5.1638-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:91c6147b9e62e42154c3211cb0164f1e561e77bf7ad8bca03c6182d828aa0f2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5154365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb963c28c8efecbf47b56dae2b0b870a39877b47a112eb2282307b5fd731d7cc`

```dockerfile
```

-	Layers:
	-	`sha256:83ab527c99c70c12d4aeeb02e29a13c55c67ced4d719ed11c8e5d49691760f5a`  
		Last Modified: Thu, 14 May 2026 23:39:33 GMT  
		Size: 5.1 MB (5140851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8cdd2a2bd7dc22af57b77dc51865b6df57cacc704a4d0a2b7b20b20f45cba4d`  
		Last Modified: Thu, 14 May 2026 23:39:32 GMT  
		Size: 13.5 KB (13514 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.5.1638-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:8714864cef07780c8f4496f599646b97ddb554188526d5032b13d80baf887785
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.1 MB (222087996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b391ac3d4725fd257a20279903d7936391d844ecf49c1200b244fc25cdc18248`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1777939200'
# Thu, 14 May 2026 23:32:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:32:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:32:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:32:15 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:32:15 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:32:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:32:35 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:32:35 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:8e45267b009b7e1018e83fd0f228ba0ad9b97aea9f10520c2d76c3baa70dfe01`  
		Last Modified: Fri, 08 May 2026 18:27:33 GMT  
		Size: 26.9 MB (26891602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e52372d5fb2e4448599149f5fdd18e1d6933ee7757f50701f6b69d3caa03696a`  
		Last Modified: Thu, 14 May 2026 23:33:05 GMT  
		Size: 126.7 MB (126651718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a2d98cbd6de606f19104ccea765ae25ba1f3864d02aed2c83452c968ed51b6`  
		Last Modified: Thu, 14 May 2026 23:33:04 GMT  
		Size: 68.5 MB (68544028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ef0b6604e65607d8f993722e38a0d65752118853a748b09539be12300129145`  
		Last Modified: Thu, 14 May 2026 23:33:02 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.5.1638-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:77e2ada12dbc3f00505768196d0ad1c4c61a6f6c313cd698e3970635b5e4c4f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5142053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e34807b4d36538218c4b987404aa1ee3619aa2987a2562b4a8dc9c1f9a7977d`

```dockerfile
```

-	Layers:
	-	`sha256:583efd56388885dbef03b71b22b7871e6255a05e3644ebc15f1c49b4db53c25f`  
		Last Modified: Thu, 14 May 2026 23:33:02 GMT  
		Size: 5.1 MB (5127633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b6ebafefb1ac5c42ce359ba07e347a21fc39126b840b508fa4e5598767ce9be`  
		Last Modified: Thu, 14 May 2026 23:33:02 GMT  
		Size: 14.4 KB (14420 bytes)  
		MIME: application/vnd.in-toto+json
