## `clojure:temurin-11-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:da34fdda382afa2d617b4217ae51ef020d9983a6ab1bb22a5669413bb3d9028d
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

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:10aa3f5586208140678207d949833434174edec2e109562197515011d065122c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.8 MB (243821866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e555ae88f114e4830f9d88eac84867eeec8eb2e1257c7b3ab0c8d4b477d9298`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 29 Apr 2026 23:15:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Apr 2026 23:15:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Apr 2026 23:15:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Apr 2026 23:15:05 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 29 Apr 2026 23:15:05 GMT
WORKDIR /tmp
# Wed, 29 Apr 2026 23:15:21 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 29 Apr 2026 23:15:21 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Apr 2026 23:15:21 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beb53236cec753f36816237591486089733b37b66d81075afc51cfec85e241c1`  
		Last Modified: Wed, 29 Apr 2026 23:15:44 GMT  
		Size: 145.9 MB (145886240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e54b60458477eb0bcb252ac5ede8f1081878490ddf41dff7238f25a49d8dd0f7`  
		Last Modified: Wed, 29 Apr 2026 23:15:42 GMT  
		Size: 69.7 MB (69698731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb6dc76a11de8aa5e4e0331bd8baac011df7780f863a64a449b7aaa515295546`  
		Last Modified: Wed, 29 Apr 2026 23:15:39 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:106903109f4bbe985796fa8b1d0b0d178e4f45538dd45274c43a094fce3e8977
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5150577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55e3f864470c2309d3297f663122701ac8f4fb7c2012a2fad15ac88a6884fe8c`

```dockerfile
```

-	Layers:
	-	`sha256:3bebb95f262cb174e89b89e7ac50de099270f881631dd96cb94463fb3a0c1a59`  
		Last Modified: Wed, 29 Apr 2026 23:15:40 GMT  
		Size: 5.1 MB (5136310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c29f686e55dbb83bd7a4a628052648866e852822be02ca15bc4fb83a63b6482f`  
		Last Modified: Wed, 29 Apr 2026 23:15:39 GMT  
		Size: 14.3 KB (14267 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6a5d1ce703393b97a8f241e95ffb169df2d36e3d66a8e2d330af922696c16462
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.4 MB (240393266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33ae40178defa1d2582de2c3226f36c4afa44fc438fd4caa12e11c63076668aa`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 29 Apr 2026 23:14:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Apr 2026 23:14:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Apr 2026 23:14:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Apr 2026 23:14:24 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 29 Apr 2026 23:14:24 GMT
WORKDIR /tmp
# Wed, 29 Apr 2026 23:14:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 29 Apr 2026 23:14:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Apr 2026 23:14:39 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:46ac7a0b9811e518f6b5a0d52940c913a1a560a8f78b82267804914e50244d2d`  
		Last Modified: Wed, 22 Apr 2026 00:16:03 GMT  
		Size: 28.1 MB (28116114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f938b9e7e55a7916d048b72300b00bec4b3be193a7078e8c611de515b33c4f6a`  
		Last Modified: Wed, 29 Apr 2026 23:15:02 GMT  
		Size: 142.6 MB (142583978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3f61832ab7651806417961e10bb65888fd6671d0ebc8339040b6ef6e2c465a`  
		Last Modified: Wed, 29 Apr 2026 23:15:00 GMT  
		Size: 69.7 MB (69692529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05325ad4ad52069f2ac6eb8aafe5a374987c0f725e3a5b733d25a85c254e2fab`  
		Last Modified: Wed, 29 Apr 2026 23:14:56 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4672a3a27e21868cc7187242c7675813e2015ac9b9ee9d4312ecf6a18007852a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5157074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83b4863a79cec94da60ae09ce332905bcfe672df5b37dbf29a1fa573072af463`

```dockerfile
```

-	Layers:
	-	`sha256:351749f9218c5bfbe0589733fbc07e4a55d0c7429e255924da3e310a8bd25289`  
		Last Modified: Wed, 29 Apr 2026 23:14:57 GMT  
		Size: 5.1 MB (5142689 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55785ba5b559e1c3d6c2f29a56dee2a163b04a26e396e06d282f48307b1805bb`  
		Last Modified: Wed, 29 Apr 2026 23:14:56 GMT  
		Size: 14.4 KB (14385 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:a85093170def7d1ad957c06f6aab624189c88da50b552136de7d712b5b6b9e51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.7 MB (240718288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a50f606f4c3aabf865e1784ce0ae09c0fc720a1f7e8216b9469effc553eac09`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1776729600'
# Wed, 29 Apr 2026 23:24:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Apr 2026 23:24:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Apr 2026 23:24:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Apr 2026 23:24:01 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 29 Apr 2026 23:24:01 GMT
WORKDIR /tmp
# Wed, 29 Apr 2026 23:30:02 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 29 Apr 2026 23:30:02 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Apr 2026 23:30:02 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:0bcb46f6315f7a2c8ddde875fca21de96c94e451046e6692f77a99aca489f3be`  
		Last Modified: Wed, 22 Apr 2026 00:15:02 GMT  
		Size: 32.1 MB (32078402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708b07913b504d6aaadb438509b6f4cb2908200d51c3b63cefa839b8f462833b`  
		Last Modified: Wed, 29 Apr 2026 23:25:32 GMT  
		Size: 133.1 MB (133109605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98de7efe3126e140f4ae4e902c0100e0f0555c6bc1fa398d20df944bf914f6ed`  
		Last Modified: Wed, 29 Apr 2026 23:30:56 GMT  
		Size: 75.5 MB (75529636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b09a5afbb051bab12476fa1add63fa95513e872e9d46f20a08500d15db7273`  
		Last Modified: Wed, 29 Apr 2026 23:30:53 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f8c8dcc98f0bb5d293f0824c02afc36dad7f0865fe7a50168013b405d3db19f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5155168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b38a646574b27bafb4ea045ad6600c4bd60b2846db00f91eb9a2640e2f2d05f5`

```dockerfile
```

-	Layers:
	-	`sha256:80cdda739748decf944e1dbae2a28423fe5088f533c893d0333effced4a8340c`  
		Last Modified: Wed, 29 Apr 2026 23:30:54 GMT  
		Size: 5.1 MB (5140853 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d502a913cbb7bbcaef4c7360b06295eda5cac6a228e3d62924d0b325e6b27ba4`  
		Last Modified: Wed, 29 Apr 2026 23:30:53 GMT  
		Size: 14.3 KB (14315 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:269d1854ac1a6add3bd4db55e5c54481f629c067b9e15512be69009d3eeb638c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.1 MB (222057948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d10fcde7a95f16a6d448e4a51c700bf86a3c32ea8bed0669beafa8278b312274`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1776729600'
# Wed, 29 Apr 2026 23:13:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Apr 2026 23:13:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Apr 2026 23:13:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Apr 2026 23:13:31 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 29 Apr 2026 23:13:31 GMT
WORKDIR /tmp
# Wed, 29 Apr 2026 23:14:38 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 29 Apr 2026 23:14:38 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Apr 2026 23:14:38 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:e579a0e0e7bfecd47e7766cad04eb36ba4b3ee329c3806a48d41d336705a1ca6`  
		Last Modified: Wed, 22 Apr 2026 00:15:36 GMT  
		Size: 26.9 MB (26891563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb51d1f6103c562773e5ad9b244bea0d905640ceeb1f8ac3e09c56a4396e5429`  
		Last Modified: Wed, 29 Apr 2026 23:14:06 GMT  
		Size: 126.7 MB (126652697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f86294f53c691cd4b8219c4529be0c37d36eb392be9fc90e6ac8d50984f52706`  
		Last Modified: Wed, 29 Apr 2026 23:15:03 GMT  
		Size: 68.5 MB (68513044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de95a012ec478b1983275d908ab3c9ad3cd434ee11d8f3d677b0f81c991ace26`  
		Last Modified: Wed, 29 Apr 2026 23:15:01 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1596fc9c88b59ef47948192cc8377544f7b3db18d8248a49870e051191e995b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5141902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfef6c15e96931f985ae60d99ee2e842d67e13f3f90ec8ce9b1469159346f2b1`

```dockerfile
```

-	Layers:
	-	`sha256:c5937094a4d11a2b48790997f652842b33af21910c016b79b5a8678f63284575`  
		Last Modified: Wed, 29 Apr 2026 23:15:01 GMT  
		Size: 5.1 MB (5127635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:496dc5c17e032e6908105a40379488fa7d8e418ea01f8d6fdbcc462a0bb53439`  
		Last Modified: Wed, 29 Apr 2026 23:15:01 GMT  
		Size: 14.3 KB (14267 bytes)  
		MIME: application/vnd.in-toto+json
