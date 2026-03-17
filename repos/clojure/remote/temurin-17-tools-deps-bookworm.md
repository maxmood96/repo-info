## `clojure:temurin-17-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:76dfdaa2009d124c15abcb463a13dac64338ffcff171c9120428da75df9319fd
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

### `clojure:temurin-17-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:33ceba3e66400140396db9952f0c28d3a7741fd84c035247d8c127685fd04b07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.3 MB (275295623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15f7d50480403d88ce2a866e22f7da0899a66dcd21dbb8f3ec3128039da0116d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 02:57:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:57:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:57:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:57:40 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 02:57:40 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 02:58:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 02:58:32 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 02:58:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 02:58:32 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 02:58:32 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9d2f29087bcd6d99efd909a99095549425cd63e27c71b3bf37f108c6b7c370f9`  
		Last Modified: Mon, 16 Mar 2026 21:52:42 GMT  
		Size: 48.5 MB (48488584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87ff8b0b9d4c1a2f510cecdd760da6095cf78c80f085e00a01311da4e729f02c`  
		Last Modified: Tue, 17 Mar 2026 02:58:12 GMT  
		Size: 145.6 MB (145628435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12fb6ad7dc43a3ba47a4f0b306f72d5d48c67d21b6789019a08af6f09c011ca6`  
		Last Modified: Tue, 17 Mar 2026 02:58:48 GMT  
		Size: 81.2 MB (81177565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c28152e97c5ba8b59af178d01191ba0a5de8e9da81283d94ded59c2f998ef73f`  
		Last Modified: Tue, 17 Mar 2026 02:58:46 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0323583ad3a6da6588ad0d075d061593c84c49f0f92ce4996a748bae0d9468f`  
		Last Modified: Tue, 17 Mar 2026 02:58:46 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:b9f0b6fee4aedde548163b842b33f4e62805a66bbce4043c8c5bf166c918d6c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7394080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6f11b102b41a157d6e8cdd182eab30b54d09554ccebddc6d8d4b3f34d727d2d`

```dockerfile
```

-	Layers:
	-	`sha256:983ed6cfc327230716663d693866fa801ef99102c9f8b11acf909ab219c38ae7`  
		Last Modified: Tue, 17 Mar 2026 02:58:47 GMT  
		Size: 7.4 MB (7378302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d997d454c6cf67d2388fe8b32a72f6a02bc8d9ef0b5b12519c6c0bae38f623ee`  
		Last Modified: Tue, 17 Mar 2026 02:58:46 GMT  
		Size: 15.8 KB (15778 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9b3a5258349c3f1033e865ccb017230bbba1dfa96a17697f728cbe7d4d52249f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.0 MB (273968657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd49c6b142b0cf75f7183c9dd7ade0ec188e2f840dca4bb58be0cd2c6ac01d68`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 03:03:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 03:03:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 03:03:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 03:03:08 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 03:03:08 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 03:03:24 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 03:03:24 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 03:03:24 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 03:03:24 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 03:03:24 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2ea98bb5eec9d02a0d7b59638c683db4e1e749f998a317bc731e9506f8480b12`  
		Last Modified: Mon, 16 Mar 2026 21:52:02 GMT  
		Size: 48.4 MB (48373032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20722c105ddf91f1823079898cb9861547e1097f2f7e25349d03526ed289b3b7`  
		Last Modified: Tue, 17 Mar 2026 03:04:11 GMT  
		Size: 144.4 MB (144436241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b760beea9030c395f704364f33be3d7bfe31f9ac5f85de681675f1ba04479a5`  
		Last Modified: Tue, 17 Mar 2026 03:04:03 GMT  
		Size: 81.2 MB (81158345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c00798b77f8ec01218dfc3053702037110ac5fd538127908bf47355dcd0f6933`  
		Last Modified: Tue, 17 Mar 2026 03:03:48 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e49d99f0c149be11fdfd9d442df8cce038e28d250d58cda396243d78ae963fc`  
		Last Modified: Tue, 17 Mar 2026 03:03:48 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:cd30cc75aab0e9773cd08b9b4b87c5ed691195f634c7e5c4b41550248862414e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7399961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07f6c42136741f1bb2c1e80078689727c216a81d32b89086ef1022f515be810d`

```dockerfile
```

-	Layers:
	-	`sha256:5b316c43acfa61d9de10ace73ef26c76fefac7d5f0956349944404ab849e66b6`  
		Last Modified: Tue, 17 Mar 2026 03:03:49 GMT  
		Size: 7.4 MB (7384065 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:600e10e48d42d5b973ddc546f227f8daa587f14d830ed9e02c2ab6eb13e6c487`  
		Last Modified: Tue, 17 Mar 2026 03:03:48 GMT  
		Size: 15.9 KB (15896 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:3e3c5342562cdf6d5fe9eb2b4e0daa6acb4eb637554f50cdbf8132e451c1e751
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.8 MB (284776130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4713a783704ddcb231c5c959682630f8363205facf1e6bc002207fb570489d3f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1771804800'
# Mon, 09 Mar 2026 20:50:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:50:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:50:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:50:52 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:50:53 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:51:40 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:51:41 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:51:42 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 09 Mar 2026 20:51:42 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 09 Mar 2026 20:51:42 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:605d3e8e339092bb5c341e87f55fee22f143aaa738eb91d341b5fc6aa27b2b5b`  
		Last Modified: Tue, 24 Feb 2026 18:41:51 GMT  
		Size: 52.3 MB (52336797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011970ecf2f315c69c83fa94ac41516957ab5211efc229c8c8c282ce6bcc7724`  
		Last Modified: Mon, 09 Mar 2026 20:52:26 GMT  
		Size: 145.4 MB (145438252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9244c828510b54f631ee1b949f0503bb32e338f1486b9b9f24cdf97930ff38b1`  
		Last Modified: Mon, 09 Mar 2026 20:52:24 GMT  
		Size: 87.0 MB (87000037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86619a29734a49cf3a9e4b3f1efa47e224d7838164aeab891673e112d692b044`  
		Last Modified: Mon, 09 Mar 2026 20:52:21 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ad578eb2bc1988599f1a1231524fc71a59f271be774a1e80b2b85826d3199b`  
		Last Modified: Mon, 09 Mar 2026 20:52:21 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:fc6863a919b6cd65b067e08077031bc413ddcc4ecf5d8ae7e739e7942f005039
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7399344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:051a2e1036278abaa26b40d2095ccdc779acb9664ed625a71989c6c9654fac44`

```dockerfile
```

-	Layers:
	-	`sha256:306003ea6919e4feb4d60c32821dabcc7aca0e4d85dc549475f263508c0933cb`  
		Last Modified: Mon, 09 Mar 2026 20:52:21 GMT  
		Size: 7.4 MB (7383518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8296d74f1cb393acaf99fa44ced797e6b8b7e59bd16273e3803c5eaa0363eb7`  
		Last Modified: Mon, 09 Mar 2026 20:52:21 GMT  
		Size: 15.8 KB (15826 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:a83096c34ef30d9e9fb79813111f573d051d17882de8c10b57309001b43f4900
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.8 MB (262765279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:198c16240690949c17f5a4e6dc7ce3909a5ec9805e7f424e3a0258dbd73edcd2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1771804800'
# Mon, 09 Mar 2026 20:33:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:33:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:33:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:33:30 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:33:30 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:33:44 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:33:44 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:33:44 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 09 Mar 2026 20:33:44 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 09 Mar 2026 20:33:44 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:00b1871f38dea81b1982e306480bd9f97cedf7b0cb3342e4bc84925e6082ade8`  
		Last Modified: Tue, 24 Feb 2026 18:41:26 GMT  
		Size: 47.1 MB (47148087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c5012ce39a9a9ae11cfc01592c6945c67dfcf71ac11d4bf491f0de2e19321dd`  
		Last Modified: Mon, 09 Mar 2026 20:34:18 GMT  
		Size: 135.6 MB (135627117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b29ea4715a609aa04f8bc24e997725a0ecbaaba901089ca2061f43494ec662`  
		Last Modified: Mon, 09 Mar 2026 20:34:17 GMT  
		Size: 80.0 MB (79989032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53e0833e8fde7c31bb7dda07c7d99ce97b682e2b366c00106c0ac3aa1a464b97`  
		Last Modified: Mon, 09 Mar 2026 20:34:14 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3332c55c8e8c28e8c31a3155076294285a06b2645dcdf3086745c75f2e8a1442`  
		Last Modified: Mon, 09 Mar 2026 20:34:14 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:d2ab5616840c78c9f42c7eb86516839407a01359667f8ddd7e08b75b3b1a44c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7385399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52b7f1502792624c793f22e201f17afd00cc88bfa14448f176d67b92378eecba`

```dockerfile
```

-	Layers:
	-	`sha256:e747ab8819650316390ab15364a6a249c4e6300f50e68eedd0f7767c56fc6ab4`  
		Last Modified: Mon, 09 Mar 2026 20:34:14 GMT  
		Size: 7.4 MB (7369621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c47d931b4bedc96e13d5e0af7ed66e5a5139cf82aaa1406add4044698c9d810`  
		Last Modified: Mon, 09 Mar 2026 20:34:14 GMT  
		Size: 15.8 KB (15778 bytes)  
		MIME: application/vnd.in-toto+json
