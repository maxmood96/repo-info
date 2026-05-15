## `clojure:temurin-17-trixie`

```console
$ docker pull clojure@sha256:02ea52847ac6c8841812f9e7561c849cbbed5244ba1f883df4d05fc458b4ef20
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

### `clojure:temurin-17-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:f4b5ac60ca99f021a98870a9699723cd4e48d31e6454cc0f3b1dbf510188bf37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.8 MB (280779200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:397c8ba2343fc0f2647c0f367d6c6c025526fa6c80482b99e28fa6bead04234f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:17:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:17:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:17:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:17:25 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 20:17:25 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:17:43 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 20:17:43 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 20:17:43 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:17:43 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:17:43 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:307f8152a55ef1e9eeb1acbbee7bc81232615329eaeb00d8dd93b46be297f34c`  
		Last Modified: Fri, 08 May 2026 18:24:07 GMT  
		Size: 49.3 MB (49302320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac1e5be7273d6b722c905e2a65e2ace602f8038be40c8073334ea51baa7c161`  
		Last Modified: Fri, 08 May 2026 20:18:04 GMT  
		Size: 145.9 MB (145905487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cfd5d1e4f94dd4fabf30e3e20a4594cf9ef16febf405043c8e39838b4e4d886`  
		Last Modified: Fri, 08 May 2026 20:18:05 GMT  
		Size: 85.6 MB (85570351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abdcc125aaea140ea64aa4e5a7bdd92ebc4ad85b442e788708cea3887dbd956f`  
		Last Modified: Fri, 08 May 2026 20:18:02 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5d046c6b8aaf1cd3a6c47ac405618e2a77296b1a0738d2b5d72a2d2ab23162f`  
		Last Modified: Fri, 08 May 2026 20:18:01 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:f7f38136e468031e1b093d474bf20ea1f31312a93da09612f72d8f2c85d1b7fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7487256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c9d63f8c91638c2f6ce9493bf33b0fbaaaf6d20b80b7a549bad96ccd2d0d48f`

```dockerfile
```

-	Layers:
	-	`sha256:fd1a33d868645f1fcdd1857b8c30405e1e529cf644e7a4d9d1a7c4bdeb411fb1`  
		Last Modified: Fri, 08 May 2026 20:18:02 GMT  
		Size: 7.5 MB (7471348 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7de2eaba3b842425786573faf14489ccff3392d346cc47f9084ce2998de4f3aa`  
		Last Modified: Fri, 08 May 2026 20:18:02 GMT  
		Size: 15.9 KB (15908 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8c584b93b17c88e756ea0b6588cd2f5d6d965be410d606990452a76fb3853b0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.8 MB (279778487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b291a88210676dd5034063c6fa1f4d07e1d5bfb32b5d2e22ca709116ae2df5c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:21:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:21:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:21:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:21:43 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 20:21:43 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:22:00 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 20:22:00 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 20:22:00 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:22:00 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:22:00 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b5d74b688654dda99557234223479d1600781c2797759908abb12a2e782ab1ad`  
		Last Modified: Fri, 08 May 2026 18:26:51 GMT  
		Size: 49.7 MB (49669445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a56c836eb6329ea86476f06021e23449f5fa9f1b68c20a0d015905f1276e5487`  
		Last Modified: Fri, 08 May 2026 20:22:24 GMT  
		Size: 144.7 MB (144724336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bc6fb48129cc6ce781f623c3e672eea574ad8e052a8fc5264d2791d5acd9f49`  
		Last Modified: Fri, 08 May 2026 20:22:22 GMT  
		Size: 85.4 MB (85383665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5322e1542faeed097ad9574fb7ceaed96732442c29b4dc424f47d76231d97559`  
		Last Modified: Fri, 08 May 2026 20:22:19 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:038e9a8bc27eae71a13eb30dbf6793c17f3fb07573e7ae2718fe2f7227fce2f7`  
		Last Modified: Fri, 08 May 2026 20:22:19 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:f40bfb794baf319d6bd8cb9834df9771bd6c41f71f693f0415742cf2721b0276
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7494404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bae396feb5aa3d529a6f77656a7330c6dd57c12ad566b6501b2f3730d2ec971`

```dockerfile
```

-	Layers:
	-	`sha256:8189bdb81b15edeafef3d07a5038c7759215ad959bc2a1b08d30c45de715f9f9`  
		Last Modified: Fri, 08 May 2026 20:22:19 GMT  
		Size: 7.5 MB (7478378 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5ca6be1961a79e536f34602ac98310efd335ef6daef30c7e9112f7611f8543d`  
		Last Modified: Fri, 08 May 2026 20:22:19 GMT  
		Size: 16.0 KB (16026 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:b5627885bf0daced2fab82f1d6071b41ff945b04cc72a70d5fd0b78cdc7c9c3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.9 MB (289876730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3312ee0b69fa93c8d5386cf1b14ba56bfe981999f153348de03c85b7491e207`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Sat, 09 May 2026 02:31:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 09 May 2026 02:31:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 09 May 2026 02:31:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 May 2026 02:31:40 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Sat, 09 May 2026 02:31:41 GMT
WORKDIR /tmp
# Sat, 09 May 2026 02:35:21 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 09 May 2026 02:35:21 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 09 May 2026 02:35:21 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 09 May 2026 02:35:21 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 09 May 2026 02:35:21 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:95ea8643a6311b39c5ca6b858ab22e7e7fb5819831b6070e3d6390a0ebf1be97`  
		Last Modified: Fri, 08 May 2026 19:46:54 GMT  
		Size: 53.1 MB (53123165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06742bfd6f3a4c91a065b055265b2edf944919541ee9c7934bc1931edc1dd4ae`  
		Last Modified: Sat, 09 May 2026 02:32:54 GMT  
		Size: 145.8 MB (145766111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e792fdc0dfb5ae5be0482f19db2eb27c5d26695f9c2815506c9c0a1fe15224ad`  
		Last Modified: Sat, 09 May 2026 02:35:57 GMT  
		Size: 91.0 MB (90986412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa1984f991609ad144af4ed0d12396ece73a3521f540ca137dd2088383fce0cc`  
		Last Modified: Sat, 09 May 2026 02:35:55 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab128744cf1b32df52a7352a74fe176e3e038ff14989c0efd5a554fe8159519`  
		Last Modified: Sat, 09 May 2026 02:35:55 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:f0bdd03c6bd7cbb4ddd355556ac8ab0b6f0eaf10e3ba95281ae821e7712e6204
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7491725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e12eea006ec7afce2a8fa658117e6e7819328cf2a72f95288e2003ad11bcad8`

```dockerfile
```

-	Layers:
	-	`sha256:9acfe42ea7435c7327d0b06a4307c612cec45295e9af1b7dcadf017708731eb9`  
		Last Modified: Sat, 09 May 2026 02:35:55 GMT  
		Size: 7.5 MB (7475769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe01c026fc513fe688f3ceb4afbbe2713d37b181c9aa0e5a81788c98c263e209`  
		Last Modified: Sat, 09 May 2026 02:35:55 GMT  
		Size: 16.0 KB (15956 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:373c16b2513ce61ee08fd1a1674939adb310b7698ddfbdf06a188c3201b6f7e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.8 MB (271828475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:680e71abddec07e869bfea629c38ea3cec3c04de5118993dff9dcf89960425f2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 22:15:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 22:15:32 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 22:15:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 22:15:32 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 22:15:32 GMT
WORKDIR /tmp
# Fri, 08 May 2026 22:16:50 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 22:16:50 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 22:16:50 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 22:16:50 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 22:16:50 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:49f5adf9d898afa33e019e0f5f9be5e639ceaf0c068ac396b0e56deed0761246`  
		Last Modified: Fri, 08 May 2026 18:29:56 GMT  
		Size: 49.4 MB (49372304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7ed7aaeed1c65fcc4999767a473cf745af3bbd97738b57ccdb46296b8107390`  
		Last Modified: Fri, 08 May 2026 22:16:12 GMT  
		Size: 135.9 MB (135910435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e43cf2b31f1549e9bdca4f4f22e9b37f459bf18037b7906a5a7ab1b26b998f3`  
		Last Modified: Fri, 08 May 2026 22:17:19 GMT  
		Size: 86.5 MB (86544695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a1dd646a5ce2cd6d2630012fac61bcefd007e40e349cd4e8a3b57f6b94e9d1`  
		Last Modified: Fri, 08 May 2026 22:17:17 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a14d4eb6cdb9e27cb2eb094fd5cb59b6cbf08e9ab295bac4ef2783e261c9e15`  
		Last Modified: Fri, 08 May 2026 22:17:17 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:043f73acb918a9453d73ae498928298aef1eeea96f4c086b749c6453b6d9c66d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7483178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d076828f1542c381253ea089b23e356aefaa62c23a6267f86fce08841a87318f`

```dockerfile
```

-	Layers:
	-	`sha256:72f835909a2e517944920d46d7f7f6beaa5f54acd7b0f1551e296c93544bcdc7`  
		Last Modified: Fri, 08 May 2026 22:17:17 GMT  
		Size: 7.5 MB (7467270 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c872e26b8ab1f8bb976235e5f6b3bd585c6862c091bb277174542167936b0a48`  
		Last Modified: Fri, 08 May 2026 22:17:17 GMT  
		Size: 15.9 KB (15908 bytes)  
		MIME: application/vnd.in-toto+json
