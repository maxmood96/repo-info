## `clojure:temurin-11-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:622f71fd4020e6f06cf0870d7df939278bec058671b9e4591d5ebdc5c01b4cf9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:8fdead77ad731877043087279bfbd26d99114f276313f45fffc746398bd14746
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.5 MB (268499732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffd9256955a87e24cf13974ac410031ead97c81dfd5a2167923d3a3adb38addc`
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
	-	`sha256:5eee3a330b5e6e63668b310d9b391ea0ba561a34d233e492a71783d6649752e3`  
		Last Modified: Tue, 03 Dec 2024 03:19:31 GMT  
		Size: 145.6 MB (145601429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:103dcc0c9db920d2bd714da0275a18b5fe740068752517a632d5ddbf2e6bfc18`  
		Last Modified: Tue, 03 Dec 2024 03:19:31 GMT  
		Size: 69.2 MB (69158511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00b21a9284f170dc18e0d85af5b6fc4746a8d7a2cc2f6fdcdddd056cf0612571`  
		Last Modified: Tue, 03 Dec 2024 03:19:30 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:b8ab42c8b8cf51f79b33132cd31936b437154c0a2f04e29d8e3d305e4a62f0bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7248490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b841c4517569ddf7f944830051ef02a6f7faed1e72bd8ff05a0befd6e215eaf7`

```dockerfile
```

-	Layers:
	-	`sha256:04f42dd2f6400cc989b64d1059f763141432236fd64aa8d10f7c336e233171db`  
		Last Modified: Tue, 03 Dec 2024 03:19:30 GMT  
		Size: 7.2 MB (7234238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a59b39b4244cc20e4b885a1e0db468e929773020f7f1bcd4e8a9d8ae1d22883e`  
		Last Modified: Tue, 03 Dec 2024 03:19:29 GMT  
		Size: 14.3 KB (14252 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:bfa55b73cb50e43991f0e26c7c7afc96e8a321acc8b57ef2912bf844a5d5e8d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.4 MB (265423045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e7f885c00c50effdf4b559c353bbcbd6813d73fd511c6520b18ab951d06ccb5`
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
	-	`sha256:b743443a1a096d0629648e4cfbd30aaf2d10c0638449f9ec92bbfb798dd4a2bf`  
		Last Modified: Sat, 16 Nov 2024 05:22:06 GMT  
		Size: 142.4 MB (142389148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a134a5935304590920d7cae3d7c2a44b1b93864833658cf703ddbe9871e914fa`  
		Last Modified: Sat, 16 Nov 2024 05:26:21 GMT  
		Size: 69.3 MB (69276181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3661dae4fc6bcb59932aa19edd64be5db245441f72e156ed06e62ac216afe406`  
		Last Modified: Sat, 16 Nov 2024 05:26:18 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:9fdec3cc72a05ccc46f1b74c62278e5a9122e329f72a16f9be8e235e84038cde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7256133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8929b8850331f1d16a6a56fbdef082f365fbd798e907ad8db3075b807ab4f954`

```dockerfile
```

-	Layers:
	-	`sha256:212927354aa9445f705c48f5415447154592398868409f50d1dfb7caef292316`  
		Last Modified: Sat, 16 Nov 2024 05:26:19 GMT  
		Size: 7.2 MB (7241763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5bed0a690a548230bf2809f5cdf0ea3843ae46fdd3a1d91b90788170bcb34b6`  
		Last Modified: Sat, 16 Nov 2024 05:26:17 GMT  
		Size: 14.4 KB (14370 bytes)  
		MIME: application/vnd.in-toto+json
