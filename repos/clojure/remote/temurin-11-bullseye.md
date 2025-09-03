## `clojure:temurin-11-bullseye`

```console
$ docker pull clojure@sha256:63ac50fe6b617d51c47cd4a683ac9c5b57324f10e26150fcbe9cb215d29a3f03
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:252348cb388361a06498642b1e1d705bf6a6351ffa1bb74cfe3670479ba64aae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.0 MB (268970865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c85ca431b6729f621842bd84543b7bd619c0810dd12b4ec24e374dd67e99872b`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:078965fc7cf303b72cc4eef5479dc2dbf5bc84fb8e6052a89b9b5362e14b3651`  
		Last Modified: Tue, 12 Aug 2025 20:44:43 GMT  
		Size: 53.8 MB (53755344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc1b375f938c9f1ad67eff1d80717f8c34ca50b82830ae94665bf4e76217ae1d`  
		Last Modified: Wed, 03 Sep 2025 09:11:30 GMT  
		Size: 145.7 MB (145658232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9c7b735378a7b2fb6425f035ce9998162676fb71bc3e16f522ef0ed2a14b11e`  
		Last Modified: Tue, 02 Sep 2025 00:17:51 GMT  
		Size: 69.6 MB (69556643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee654f7929fa46b4ed8b2445398675a6170f7ef34ba55cfbf0f4570330cd46d`  
		Last Modified: Tue, 02 Sep 2025 00:17:40 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:1a1a17551ae6ec12c8a450fd314e47f6b2a5db532d1e471e2f46f3a736ca2927
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7430060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aebe2516630d64774163ee0070c89776cb2802559acdcbba41110e2c4a41ec9`

```dockerfile
```

-	Layers:
	-	`sha256:a32c8ce23ef77a90f69875e7bd32974f903cb492d9de9c068a2bb3d9b08cccf1`  
		Last Modified: Tue, 02 Sep 2025 03:35:33 GMT  
		Size: 7.4 MB (7415808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b3ecb9f2d16c834f00fd2d3bf06321cc59b022a66c0573413c5f91635694b45`  
		Last Modified: Tue, 02 Sep 2025 03:35:34 GMT  
		Size: 14.3 KB (14252 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:44362820d662c43ccca38a524850952e78806631b11d33bf95f5e01d32dd4845
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.4 MB (264392204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c72d3c730bbf625a2b736e167de9c32fe5a6a329bcfb7301cb56dd538afc4383`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:7b68ea47bc3cd8615e51fdbe0976cb4999ba56ce8764e755543a4521d69a32f6`  
		Last Modified: Tue, 12 Aug 2025 22:08:57 GMT  
		Size: 52.2 MB (52248409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9c7add852716fa73be85d031a79e4c2ff9fbc90a7ff1431cc0a18d73fd1e50f`  
		Last Modified: Wed, 03 Sep 2025 09:12:22 GMT  
		Size: 142.5 MB (142459084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a55d6b93e1648b21fe9f6dbe81cdd9ad1e11d6be09e48998cd0feb48ca90be2`  
		Last Modified: Tue, 02 Sep 2025 07:53:20 GMT  
		Size: 69.7 MB (69684066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:273da56c9e975f28dd93630ab3fe87a19c02a73ca659e479cf6cfec74979bb1e`  
		Last Modified: Tue, 02 Sep 2025 07:53:12 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:441e01d1db0621599bd5e286bf8679108777debd07824224a04abc49c4260793
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7435895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3bcc12a900280331e0c428f9970335f7354a7510b0a8ac20a5889bbaeae0c0f`

```dockerfile
```

-	Layers:
	-	`sha256:89d172e74bce7f2fa4bdc5c6fb35989a716cf13cd1c4245606363f64acd3b6ce`  
		Last Modified: Tue, 02 Sep 2025 09:35:37 GMT  
		Size: 7.4 MB (7421525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa5b6fb2189cef7f7ec763edf16e64cc66de81c15ac0143861d141ee0b3463f8`  
		Last Modified: Tue, 02 Sep 2025 09:35:37 GMT  
		Size: 14.4 KB (14370 bytes)  
		MIME: application/vnd.in-toto+json
