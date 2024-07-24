## `clojure:temurin-11-tools-deps-1.11.3.1456-bookworm-slim`

```console
$ docker pull clojure@sha256:3934ac8e932fd7bc9cf69906a41445dfaca7dcde38553a0c3f3988ed323446cb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.11.3.1456-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:a3cc6a0e53bfda2e7309bde799807039427c3cc1ea93c2eb5277b87aab971513
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.7 MB (243744788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dced7021dd1578a54198bbca9fcbf5ff75ebfa1462256300f8be214f76279184`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 20 Jul 2024 21:06:39 GMT
ADD file:6c4730e7b12278bc7eb83b3b9d659437c92c42fc7ee70922ae8c4bebfb56a602 in / 
# Sat, 20 Jul 2024 21:06:39 GMT
CMD ["bash"]
# Sat, 20 Jul 2024 21:06:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 20 Jul 2024 21:06:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 20 Jul 2024 21:06:39 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Sat, 20 Jul 2024 21:06:39 GMT
WORKDIR /tmp
# Sat, 20 Jul 2024 21:06:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:efc2b5ad9eec05befa54239d53feeae3569ccbef689aa5e5dbfc25da6c4df559`  
		Last Modified: Tue, 23 Jul 2024 05:27:55 GMT  
		Size: 29.1 MB (29126287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:931fadb73c06ce2d1faf10311bb134d55e9ad7d0b7c5350f0955532da9dc4dc2`  
		Last Modified: Wed, 24 Jul 2024 03:04:24 GMT  
		Size: 145.6 MB (145550342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae10f66679b260b894c0d6f68d265d83e050a838f7cec55db7720bd0272d8893`  
		Last Modified: Wed, 24 Jul 2024 03:04:23 GMT  
		Size: 69.1 MB (69067512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:169bed1585621ea0e6b73bc7e4f6535cf2df8e829abf78e10cd4258ff8cf21e5`  
		Last Modified: Wed, 24 Jul 2024 03:04:22 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.11.3.1456-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:43aca3be50b2cf95fa60b0006969bd654540d99aaf5e7ade61c30f78cbdd15f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4759102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:609ded64ba29fc49d8239808d0dab0ae513abf1a5c11eaad7ddab636352f8c6b`

```dockerfile
```

-	Layers:
	-	`sha256:2c88685a031a5c4ce2e5f9209ffe95e81b2b3537e4bb71f7631fc2ca52b0f36a`  
		Last Modified: Wed, 24 Jul 2024 03:04:22 GMT  
		Size: 4.7 MB (4745164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03c5ea12fbe0da6801aa3af88fe19d4dca7089e3f9bba2b449c5ec815a00725f`  
		Last Modified: Wed, 24 Jul 2024 03:04:22 GMT  
		Size: 13.9 KB (13938 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.11.3.1456-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:057555520ef818c26c7f6d40caa7e409c455ddf1658fda5f12d22fefd2f042c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.3 MB (240331859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e98afab2426012150663f8d051c984ad658588484b5875a5a8ee3f8fc48b7c7`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 20 Jul 2024 21:06:39 GMT
ADD file:9b9556e1f3168a82eb85577dc07d85b2e7c1a72c5c35a4003f00042dd27b4fa2 in / 
# Sat, 20 Jul 2024 21:06:39 GMT
CMD ["bash"]
# Sat, 20 Jul 2024 21:06:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 20 Jul 2024 21:06:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 20 Jul 2024 21:06:39 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Sat, 20 Jul 2024 21:06:39 GMT
WORKDIR /tmp
# Sat, 20 Jul 2024 21:06:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:262a5f25eec7a7daccd94a64695e41acca5262f481c3630ef31289616897aa40`  
		Last Modified: Tue, 23 Jul 2024 04:20:29 GMT  
		Size: 29.2 MB (29156571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0044c6bef07efe98365d4134f1e7365a1e3909e34e33fb33d8bfe3e8273ce26f`  
		Last Modified: Wed, 24 Jul 2024 11:25:48 GMT  
		Size: 142.4 MB (142356420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a5fecde77b0062374986c6177b55a0edae31062d1b349e97fae25c0bba7181`  
		Last Modified: Wed, 24 Jul 2024 11:31:35 GMT  
		Size: 68.8 MB (68818219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e07415791078e4b236a2fe290a8532a37946d0ae3cedbd2ad1ae528855454605`  
		Last Modified: Wed, 24 Jul 2024 11:31:33 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.11.3.1456-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8a445fb945affa83659147ca793ad8015b689f9d626ca2b7b590be1bafe14624
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4766027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8220a39b97873ffae944a14bd488489b1d84e434ecfa29fb4783537ec6a291f4`

```dockerfile
```

-	Layers:
	-	`sha256:42ec9ec0a67bd2706c1e27c4e348da5b8b3b6ec22786487274972e3d68f838ca`  
		Last Modified: Wed, 24 Jul 2024 11:31:33 GMT  
		Size: 4.8 MB (4751549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d07fe3beb0218e771bfad36aba10ef1657c33bdfa0251ba5a4be0fcbac81657b`  
		Last Modified: Wed, 24 Jul 2024 11:31:33 GMT  
		Size: 14.5 KB (14478 bytes)  
		MIME: application/vnd.in-toto+json
