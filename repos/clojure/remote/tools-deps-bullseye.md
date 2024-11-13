## `clojure:tools-deps-bullseye`

```console
$ docker pull clojure@sha256:7bbc3b3bcf94aa6de31a1ed4f5613b6cb9779294ac457d5c847d34071961768e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:5def7dc5d081209ee67e17142b65e27cbec401ebaaae6b31b9e616b592c6743c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.8 MB (281816979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98a2b13d2440e21621d50401f2f7a349307f467985a765730ca53270abc21dc3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c2056d933cd629f55ac55802dda223f122286bf60ec42a24f0d0f6ae2615315c`  
		Last Modified: Tue, 12 Nov 2024 00:55:16 GMT  
		Size: 55.1 MB (55108780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5a20a48b0cec7d3bd3962ead3b379527c4cbe34db0cebb7872c357a9533e26a`  
		Last Modified: Tue, 12 Nov 2024 02:49:35 GMT  
		Size: 157.6 MB (157568719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12bb004160a868de854552856693edd439fd2f57b3245b5caf1742630519a69a`  
		Last Modified: Tue, 12 Nov 2024 02:49:34 GMT  
		Size: 69.1 MB (69138442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2722958bcbc5bc9bfe5ccda9cb5f86757a74ce0c0fac764b2b6cce3af30f19b`  
		Last Modified: Tue, 12 Nov 2024 02:49:33 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d0676ed45cd48c1e4e09da26d4ef790c998fef5ffe3e688a0923635652f219`  
		Last Modified: Tue, 12 Nov 2024 02:49:33 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:aa58b60106ebd56fe54f9b198605684128a11b6d5f945dfa59150cb45c4226ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7236150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e6e1cfb2f32148aafe405569498978308a563afe7c80642ca3e6ac4e3e1b601`

```dockerfile
```

-	Layers:
	-	`sha256:0c4c631e2f692f2801606bfd0ad95bf98388ccd8a4bf534903bd3ea103dd502f`  
		Last Modified: Tue, 12 Nov 2024 02:49:33 GMT  
		Size: 7.2 MB (7219653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:175b54051b0f71d252996ea736a024a32798779e3af3a9f007d902c70510203b`  
		Last Modified: Tue, 12 Nov 2024 02:49:33 GMT  
		Size: 16.5 KB (16497 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ff8906cbcbbda4201a957811848cf606128b826d385956d118122b02fcc4fba7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.8 MB (278828176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23e69cdddf7659f687f94ae602bfa79cdf7b97d6121f85216ac1c240b0a61549`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a839664fe62f615da74af799f94ccbc890a15d0f78470aac54302c2fd5475615`  
		Last Modified: Tue, 12 Nov 2024 00:57:41 GMT  
		Size: 53.8 MB (53757072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6bb1496b0882c6bf50fa016667b9de7ba874e018c7631377061fa59f267f42f`  
		Last Modified: Wed, 13 Nov 2024 01:27:25 GMT  
		Size: 155.8 MB (155793073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b607bf8a08f2eea5e3ec78ba3e87b2e69313c4f7e4248beff0d57fdc226590d`  
		Last Modified: Wed, 13 Nov 2024 01:31:24 GMT  
		Size: 69.3 MB (69276992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e35f33671ed8c8365545ad28e3cd7cde6a59cadcf4ab77e9200fec596e219652`  
		Last Modified: Wed, 13 Nov 2024 01:31:22 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c196c51b2d12d6fe08e6c3766231c60584a87e25bb91c4c90c1cb3752353a4`  
		Last Modified: Wed, 13 Nov 2024 01:31:22 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:18c49f233e5fec005abe08a2a29d89747612143885c6c6889e2dfaae387160f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7241419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b18842aa61ee83e9ee48b0cfdd7f8835d0b1faf93ad9e7c05af1204adcb239a`

```dockerfile
```

-	Layers:
	-	`sha256:ade3a5e5d9b2ac9f0e43df72ee7c0412aad3960f946cfc3451f697e57247903f`  
		Last Modified: Wed, 13 Nov 2024 01:31:23 GMT  
		Size: 7.2 MB (7224780 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:068379994190fc5adf6f807bd5849e66fb446dc16a5c8b1f4f19bc86fff4d28e`  
		Last Modified: Wed, 13 Nov 2024 01:31:22 GMT  
		Size: 16.6 KB (16639 bytes)  
		MIME: application/vnd.in-toto+json
