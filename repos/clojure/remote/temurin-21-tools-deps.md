## `clojure:temurin-21-tools-deps`

```console
$ docker pull clojure@sha256:36f0f6c2919486899a7033f770cadd3871cb5a1ea821a7d23ffcb1eff89872cb
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

### `clojure:temurin-21-tools-deps` - linux; amd64

```console
$ docker pull clojure@sha256:14f1d037ddb9c1feb332036dcff572f1733888b526f752cfea1ea377a6ddcd57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.5 MB (287513099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ef198425e0182deb4d7189225b9fa4d304851e23fc675b91282a3cebf1ffb72`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:19:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:19:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:19:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:19:52 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:19:52 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:20:05 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:20:05 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:20:05 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:20:05 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:20:05 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:db53381ee51f9e43304e236099ba097ae1b33ae41a8007e0b6319992eb55fd00`  
		Last Modified: Wed, 22 Apr 2026 00:15:45 GMT  
		Size: 48.5 MB (48488628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d481bac3cb68cfc946c2db6bf5993730fcd8837abe8b8587304aa8c4462fddc3`  
		Last Modified: Wed, 22 Apr 2026 02:20:29 GMT  
		Size: 157.9 MB (157857071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a8c4ecdce35666780600c1912c6bab3605f04440387debf4c1991adbaa67dc`  
		Last Modified: Wed, 22 Apr 2026 02:20:27 GMT  
		Size: 81.2 MB (81166362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a07c42df665f9c134169f47847a94b9000ee25fe7188764cbce1587068b3df4`  
		Last Modified: Wed, 22 Apr 2026 02:20:23 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5118e3e77b5f20161b657a69c0d4c9679dc1f09c93d4850eaff4f120a5a19c35`  
		Last Modified: Wed, 22 Apr 2026 02:20:24 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:c2067ea7cbb520288e673f099150d85bec27c6e373b95488ce5d6bf13d170b47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7397300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51b887bdd37980619ccc077dda715047edaf5abb5f098ec33ba46810c43fad80`

```dockerfile
```

-	Layers:
	-	`sha256:b1465063a9e188e674420014b1cca076f330139449856aff113c167c9a8cbef1`  
		Last Modified: Wed, 22 Apr 2026 02:20:24 GMT  
		Size: 7.4 MB (7380838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7288a0c8fc7fbbba0e42a1ccade98dd189edefb48a9d45fa1c3fee75ab5fbecb`  
		Last Modified: Wed, 22 Apr 2026 02:20:23 GMT  
		Size: 16.5 KB (16462 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e40ce6e34a5cb21decd7f0aebbed8b127c9ae676886d02ad7f3eb90c410e0f0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.7 MB (285681118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d905073abfac58e6ac67a22610ee75f79046bb7b1dc3da2a3811a10b0b951e9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:22:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:22:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:22:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:22:37 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:22:37 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:22:53 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:22:53 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:22:53 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:22:53 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:22:53 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:30de66f8fdafab67e88d876087f571a693a1a6c4cf0abc29efbf88ea878e0d29`  
		Last Modified: Wed, 22 Apr 2026 00:15:43 GMT  
		Size: 48.4 MB (48373071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c53690ce3950c4cd675924c987919f780580f2a9c61ac8352c925fa02cd54cd5`  
		Last Modified: Wed, 22 Apr 2026 02:23:17 GMT  
		Size: 156.1 MB (156133067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f8c7276b6c8159912781f9c412fa67d388222fce123ee60fa8917dd0ac2d686`  
		Last Modified: Wed, 22 Apr 2026 02:23:15 GMT  
		Size: 81.2 MB (81173939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0312b9004763d68b2041c285616a3b08b0bca4186387957e320e206657d1fa9`  
		Last Modified: Wed, 22 Apr 2026 02:23:12 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5958bd28c3508a90928a4f861d20464d97e189e0183bd9d94e0216409a420ef5`  
		Last Modified: Wed, 22 Apr 2026 02:23:12 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:433cdf32af368be19ddb668355e1011b92dafd84d5d86b8069c66344783bb615
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7403229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e963daa4380087fe0393522f388e87e1b4c4ad94529a31f6a8bf219bb54258c5`

```dockerfile
```

-	Layers:
	-	`sha256:0f5fbd9d8214aa35b0d289ac0e493ebcfaef42f411c725ba03e6cd97112252ad`  
		Last Modified: Wed, 22 Apr 2026 02:23:12 GMT  
		Size: 7.4 MB (7386625 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2de4842e8bbd53e5f88dc5cc140b8e89f3ba1345db6f5bc74f8d9cc31b071b0e`  
		Last Modified: Wed, 22 Apr 2026 02:23:12 GMT  
		Size: 16.6 KB (16604 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps` - linux; ppc64le

```console
$ docker pull clojure@sha256:cd471b2de0150752153ae3fb47beafc32527619e0ed7f33997f1276fd48497f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297319703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d8dfebd0009f7744c8e16f9da6b7a06cb020f233a502167a7b203b960e9c5ba`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1775433600'
# Thu, 16 Apr 2026 02:58:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 02:58:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 02:58:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 02:58:26 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 16 Apr 2026 02:58:27 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 03:04:28 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 16 Apr 2026 03:04:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 16 Apr 2026 03:04:30 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 16 Apr 2026 03:04:30 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 16 Apr 2026 03:04:30 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6b775f7ad22043f8bb75d535d8a1279e43453a08a4a9e6a0b48c020c9b387079`  
		Last Modified: Tue, 07 Apr 2026 00:09:43 GMT  
		Size: 52.3 MB (52336938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1250e3e4882e6e928fe5b248de7b760cd787cd434e4a4d31f63aa8ed6c00e040`  
		Last Modified: Thu, 16 Apr 2026 02:59:56 GMT  
		Size: 158.0 MB (157977483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e1679c7fc0758ed24a902d450880b010120f98cb0320d8ef6250007b191c4b`  
		Last Modified: Thu, 16 Apr 2026 03:05:09 GMT  
		Size: 87.0 MB (87004239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25b81ad85740b10f8ab8bd819a208d7d2e499abf0803ce9313c0654afcd08ece`  
		Last Modified: Thu, 16 Apr 2026 03:05:05 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48c4482b634ceb998e5383955076f3d7481eb902d240dcb2d39a7eff50b3c2ad`  
		Last Modified: Thu, 16 Apr 2026 03:05:05 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:00c8644f7b8aca84bc06eec1cd587b11d35f11b4ede01c8d61e089fac602911a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7402588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:427e567b54b1f802d0da3d3644ad66301ec195bb9d361110f664d278b205e0b3`

```dockerfile
```

-	Layers:
	-	`sha256:4954f32d5e27968b16695d9e486e8fcd26e92d44f55434a708334bb66de6e695`  
		Last Modified: Thu, 16 Apr 2026 03:05:07 GMT  
		Size: 7.4 MB (7386066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0aa52ffa0dc24ea2edf0e612eb3d21fd0e0b0737e9361545f7678f0a72a018fb`  
		Last Modified: Thu, 16 Apr 2026 03:05:07 GMT  
		Size: 16.5 KB (16522 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps` - linux; s390x

```console
$ docker pull clojure@sha256:001f4ccee57ca38eebaa835e27d8cb1ad2e7e3877ee039efd21814a1415ca153
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.2 MB (274234018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad45bbd309a2b88aa114b612718ac5a7fbf072b8c94e7d3cfbbff8da46876104`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 04:02:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 04:02:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 04:02:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 04:02:51 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 04:02:51 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 04:04:05 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 04:04:05 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 04:04:05 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 04:04:05 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 04:04:05 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:65a8acd2327b0f3316fe8707ebd5c99b15e79306d4eca71f3e635588795ae2bb`  
		Last Modified: Wed, 22 Apr 2026 00:15:31 GMT  
		Size: 47.1 MB (47147970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:823a94a034a486e2e5ad070f6a03cf5992927682e92a4d8ac4bb69d1ed8dc2bb`  
		Last Modified: Wed, 22 Apr 2026 04:03:34 GMT  
		Size: 147.1 MB (147105251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aebb546e2f387a309f6a68b4fd8ba56b7cc10be20933a9f675624598b7adac6`  
		Last Modified: Wed, 22 Apr 2026 04:04:32 GMT  
		Size: 80.0 MB (79979758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4140d0b1dfa405bc46b45e731cc6579693be9f9027e042f28d3b92910fbbe380`  
		Last Modified: Wed, 22 Apr 2026 04:04:30 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37d63b4fe7ec385b141b782f5a781be94af52353d834d6dbf34763c3c515b6a2`  
		Last Modified: Wed, 22 Apr 2026 04:04:30 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:1b925f66140c899296ef697ac6592077943e244ce5eef30a00f8b84708d12e15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7388619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e94b9bc0fae2fb53712b01bf011468d33dccded7b504dbeece6e8ad1e873953f`

```dockerfile
```

-	Layers:
	-	`sha256:8f2de666a2a170cb1cd7d9e27260b182085dc33f82fb5b0b8afb6891c849ab88`  
		Last Modified: Wed, 22 Apr 2026 04:04:30 GMT  
		Size: 7.4 MB (7372157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c5bb700f1e1b8df6c632d5c47b2fe8a3da9b6c222472b6515639bbfefb52d6a`  
		Last Modified: Wed, 22 Apr 2026 04:04:30 GMT  
		Size: 16.5 KB (16462 bytes)  
		MIME: application/vnd.in-toto+json
