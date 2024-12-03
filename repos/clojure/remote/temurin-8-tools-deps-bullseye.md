## `clojure:temurin-8-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:d5e9cccb2982e178df9fb7c76f6858b0c0ced08986aada27ad239f9106253dc1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:1fe7adb246521e0eb7e48cf8ae404bc23b5f9effe0c38cb3d10e947d49e5c000
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.5 MB (226533387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efa2ab556b7b33c66e3cf9007c7581a2edba9ce4b0d661bf770025a61a053aba`
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
	-	`sha256:cd606f6f489eb66f1307280aec321b3af3aa998dca447ae1cc91c6b884240064`  
		Last Modified: Tue, 03 Dec 2024 01:27:20 GMT  
		Size: 53.7 MB (53739147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ca8966aeb86a9f0f11248f158d2913f90028c840e94761e5f02c967158eee82`  
		Last Modified: Tue, 03 Dec 2024 03:19:31 GMT  
		Size: 103.6 MB (103633965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cfb46e616beea53e8dae140de55f9bff236e6eddae30b9f5616e11f519e93e8`  
		Last Modified: Tue, 03 Dec 2024 03:19:31 GMT  
		Size: 69.2 MB (69159631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7609a4aea1eb56d952a57a226d10c8a35136bf905dab226d29cf0fc515f7ff60`  
		Last Modified: Tue, 03 Dec 2024 03:19:28 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:1c69acd8f7d524da40bb64df3a9b993fcf9bd11da7418e4d8f9092d3c86e9438
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7350479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c8afd3f8263409f211d9318b39440d1c6246599cc96378c713117e3f5791891`

```dockerfile
```

-	Layers:
	-	`sha256:ebb27afe2e8f7bd446b939793d24a40391327a7b4801e59ec090616d5162269b`  
		Last Modified: Tue, 03 Dec 2024 03:19:29 GMT  
		Size: 7.3 MB (7336237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9a2b7ad8b4a1a3c1e4d3d8a14271938a486dec4e4297aa144ef14bb417d8763`  
		Last Modified: Tue, 03 Dec 2024 03:19:28 GMT  
		Size: 14.2 KB (14242 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f4ae0fa6d232e71b7e5a101537a07b06d0acc1a8d35ce05d07a8c4022578c1ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.8 MB (225781698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:038a742611895c321db63ba6e261f5879377ad486f5a59d80c7d495156587000`
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
	-	`sha256:a839664fe62f615da74af799f94ccbc890a15d0f78470aac54302c2fd5475615`  
		Last Modified: Tue, 12 Nov 2024 00:57:41 GMT  
		Size: 53.8 MB (53757072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feefd6a247880c6e3044381c4f7978a1eb973d63cd6342d8f7beb5de7f84e18c`  
		Last Modified: Sat, 16 Nov 2024 05:13:03 GMT  
		Size: 102.7 MB (102747729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a53de83d3262242e720cd2d0fdd5bbfcaf635dc8ee55bc1751fa62233b763f9`  
		Last Modified: Sat, 16 Nov 2024 05:17:27 GMT  
		Size: 69.3 MB (69276256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34be34dc4cce404d2b7b8187c0ec9b0517575066df4ff952ab337ad42c4ca156`  
		Last Modified: Sat, 16 Nov 2024 05:17:24 GMT  
		Size: 609.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:8e1e47cf222e94261003df7aa5d9047db02d0847edf5eb90bbc2bb130556b37f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7358201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7733a98d5d31c00bdc63a7ad0257f6db266bce525b79582d1e0c5ec5b50e5bd0`

```dockerfile
```

-	Layers:
	-	`sha256:c0167716a68fd8ad892b5fe8a4a9f50c4f4bf2de7f3235604df890d6e3582292`  
		Last Modified: Sat, 16 Nov 2024 05:17:25 GMT  
		Size: 7.3 MB (7343842 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a14cad80392f5af9b4d09e0067f6b63b8f48f4949b9b3b778841c368764753d3`  
		Last Modified: Sat, 16 Nov 2024 05:17:24 GMT  
		Size: 14.4 KB (14359 bytes)  
		MIME: application/vnd.in-toto+json
