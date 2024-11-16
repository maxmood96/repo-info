## `clojure:temurin-11-tools-deps-1.12.0.1479-bullseye-slim`

```console
$ docker pull clojure@sha256:268a88ae0b787b4f039c4be3b4c6edb2413bd1e68a8233126279069f9c5be7a3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.0.1479-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:50c38376cddbe8d7f17699b63073b42d6d352f2d806f4449895f1ba05f231a1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.8 MB (235793592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c207491cf7e75c980fade11242bfade3b5857e65ac66f7d56da85e1c8cd0e052`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD rootfs.tar.xz / # buildkit
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21aaa89a72937ffb8845d44cb7b18c5d3f00d6966117b6440324742f04415b60`  
		Last Modified: Sat, 16 Nov 2024 03:51:38 GMT  
		Size: 145.6 MB (145601371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cf29e71d9b6ab172fcfdb792fb3b9a99830660a1ba52da70a2e197701cf9b37`  
		Last Modified: Sat, 16 Nov 2024 03:51:37 GMT  
		Size: 58.7 MB (58740014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef08189ac2f26f6afb7aee5d4a9ead8c5a3365ecff0cbbe82d154f39c084d10c`  
		Last Modified: Sat, 16 Nov 2024 03:51:36 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.0.1479-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c2e796c4740c84af3f4e8746092c3b352116363ac9a42030b901c0227c0fd605
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5159833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f490b1f479ba20311e038f6a64bb6c6d81494d53ada0c7e05330753c1f610cc`

```dockerfile
```

-	Layers:
	-	`sha256:1e297d0818aff6340c461179d3214436f15ab866a9bb5eed66b2a58226c7bc01`  
		Last Modified: Sat, 16 Nov 2024 03:51:36 GMT  
		Size: 5.1 MB (5145523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88629e18279a9d54df503ae6c806142695f151637559175f14f0efd72d40ab93`  
		Last Modified: Sat, 16 Nov 2024 03:51:36 GMT  
		Size: 14.3 KB (14310 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.0.1479-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4eaa5d9023eaa175a6d7dbf0281449c8381d5b374257703156bbd39afe908297
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.4 MB (231357757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd447b088e932c209ce0d9c0a1977f1c68565b1c79fe1d942334793b12ff5220`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD rootfs.tar.xz / # buildkit
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e006532f22d92e9d5637b1cc7ac1a8afef6c6963132343754ef28d006467ca3`  
		Last Modified: Sat, 16 Nov 2024 04:39:49 GMT  
		Size: 142.4 MB (142389148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:220981c9bb1734fe52c62df37dd1508063b8946169bd1afb3054d9574827737f`  
		Last Modified: Sat, 16 Nov 2024 05:27:07 GMT  
		Size: 58.9 MB (58876365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bdb7f27c01bfe35669e2eda35c0de43deb851f0987c155a7ee6cfd976875978`  
		Last Modified: Sat, 16 Nov 2024 05:27:05 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.0.1479-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9803c8af19a0346f6f8d3aa693b32c97632417ddab07377ecd137b69483fa92a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5166307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90b63b7d726881e35c159f9d639a1af51f3972c423d68ac2c1359af190e02509`

```dockerfile
```

-	Layers:
	-	`sha256:c450ccb5999ee114459386f6ff01d175f59edd7fac6c556c2b62e50fd83541c5`  
		Last Modified: Sat, 16 Nov 2024 05:27:06 GMT  
		Size: 5.2 MB (5151879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:139f52d364198d108b16b6ad2632c9f6c0d8c3cd3c3866eeca01194b40e2eed2`  
		Last Modified: Sat, 16 Nov 2024 05:27:05 GMT  
		Size: 14.4 KB (14428 bytes)  
		MIME: application/vnd.in-toto+json
