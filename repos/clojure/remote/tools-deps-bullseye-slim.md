## `clojure:tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:0cd232b5dd272e1219ddf788abb0069e4fefde9bc29e5428de8e550eec58d2f8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:1d3c2af8585d75f41c84236c035a0c1ad89d5867bcc4396ca4974704af5e9d43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.9 MB (248949274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77a4e234d6b4fe5b04652fe0509cb1b237d6dc86514b1beb01885e228074b0bc`
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
	-	`sha256:f7286d488f1fccdf17634c3ed2f4e10a4d10c8c1ffc8cedeff6033be2465e7b5`  
		Last Modified: Thu, 17 Oct 2024 01:13:40 GMT  
		Size: 158.6 MB (158579255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e17f61d3180448d81dfa943f399cd35e408f08e1b70a7cc0c73f59c22f6092`  
		Last Modified: Thu, 17 Oct 2024 01:13:39 GMT  
		Size: 58.9 MB (58940182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff94bd3688e421e36baebfbad65bf7d96dfe5c4a58b0fd1476bbddbd93d30f8c`  
		Last Modified: Thu, 17 Oct 2024 01:13:38 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b4d21bc1709ae0169c40fa1c2e97c34ab538107d16e594aac8a66d1a454fafe`  
		Last Modified: Thu, 17 Oct 2024 01:13:38 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4667eb4bacd1da456ead04a5badd12677afbcc2e45d13c27c493df9ffc1deafb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5119619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14d89abed3366f0df95a16211f549ecc24341c1b61c175d4f21ee1fb2d67325b`

```dockerfile
```

-	Layers:
	-	`sha256:544a998cd392be340a0d67a2ea79384c0193ebff340bb3a17fa89a9f2da3dbde`  
		Last Modified: Thu, 17 Oct 2024 01:13:38 GMT  
		Size: 5.1 MB (5103372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3b1e9b3d48f2e0e834f9348533a0637e7743e7982316448b517451c5b783824`  
		Last Modified: Thu, 17 Oct 2024 01:13:38 GMT  
		Size: 16.2 KB (16247 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d34c829f22128238645e24bea29bd37b7e778b6630f1b31802689e0eae98afd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.9 MB (245895701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c34b34d17d8144a891a41380ae3208fa87481fd39207aa16aa9feace05b7c572`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:32 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Fri, 27 Sep 2024 04:38:32 GMT
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
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75d8e0685c3f988ae916e88e6ecba4356a7500cf551218d3a0ac32b094d00f8e`  
		Last Modified: Sat, 12 Oct 2024 01:24:50 GMT  
		Size: 156.7 MB (156746190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfa4d42c0e6f58e3b715798bc77e58a11482e5e6c3d20d75a33fd885d5c90b5b`  
		Last Modified: Sat, 12 Oct 2024 01:29:49 GMT  
		Size: 59.1 MB (59073308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4d616670c805f6dc23a58cab0f113882ff5a71339cc675e6c02d3a4159969e4`  
		Last Modified: Sat, 12 Oct 2024 01:29:47 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ecdee94cc1f5280177485e23e6103e73119383bc41577f589ceb74dd2ae9df6`  
		Last Modified: Sat, 12 Oct 2024 01:29:47 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c5b9cd5dd286b43b6a3024b0a1e6293aff7024280fb64239fd680eb60a9a467a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5125419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:065b70384458136f0db455fa4fdae8127e6d7e706bda4e35efd07eabaaf8dd7a`

```dockerfile
```

-	Layers:
	-	`sha256:a8733aabdb06387ac9c0941d43d7e8257f9a12fac68a9a372ea6487513a93cd8`  
		Last Modified: Wed, 16 Oct 2024 02:36:59 GMT  
		Size: 5.1 MB (5109043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:433132fb508e9caaa9e7d21cf0f3372a63f6090fe3311419f1d51a2949d91ac7`  
		Last Modified: Wed, 16 Oct 2024 02:36:59 GMT  
		Size: 16.4 KB (16376 bytes)  
		MIME: application/vnd.in-toto+json
