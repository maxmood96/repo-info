## `clojure:temurin-11-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:bf109daffbceeef23d1c0967b991e53958963d5a9aceffa467ce78ccab889cca
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:6c13fb4f297c9360c23c052af8b10121798e0babffcaf278b453901f855bf91e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.6 MB (234611003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25660139c55444c81cd7b28e87b8c8ca5d9e028672f7e0392242975902b4e052`
-	Default Command: `["clj"]`

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
CMD ["clj"]
```

-	Layers:
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02c2c9542d83778e902bdbe34ec8e5bca515a9789b979131ed96c36a4ebfa8ba`  
		Last Modified: Tue, 03 Dec 2024 03:19:43 GMT  
		Size: 145.6 MB (145601457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba3d01a9047726f3765e75a257c777ff8b1e072f0675c222936ad830f49558f3`  
		Last Modified: Tue, 03 Dec 2024 03:19:42 GMT  
		Size: 58.8 MB (58756257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32e0413525753ce7908331a6b0568e6df4727f7e61fb7a3f77b4be87d9e79fd`  
		Last Modified: Tue, 03 Dec 2024 03:19:41 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:fcf47ea5e4aa8c9361f339cd8caf789eb7c4b2e7da4f2dde2640bba0331f8bd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5158030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dccde571549d525177668f88b29a9ec746ed57146710c657fe8bdb8782ac1b0`

```dockerfile
```

-	Layers:
	-	`sha256:abc9d652c35572326ce7be40ddb363c37934e8bfeefd179c59077b5108dd7ea4`  
		Last Modified: Tue, 03 Dec 2024 03:19:41 GMT  
		Size: 5.1 MB (5143720 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4652e28ea9a77bcb0064061d905516b37e00efa4379184d9689a06101dc90fa0`  
		Last Modified: Tue, 03 Dec 2024 03:19:41 GMT  
		Size: 14.3 KB (14310 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bullseye-slim` - linux; arm64 variant v8

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

### `clojure:temurin-11-tools-deps-bullseye-slim` - unknown; unknown

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
