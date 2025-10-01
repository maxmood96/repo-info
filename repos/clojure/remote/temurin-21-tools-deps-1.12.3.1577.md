## `clojure:temurin-21-tools-deps-1.12.3.1577`

```console
$ docker pull clojure@sha256:640ad16f649c854b7b4bbce8ad3c7bcc6b9ade0ee2e268fe7b9a2d6c633a4d62
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

### `clojure:temurin-21-tools-deps-1.12.3.1577` - linux; amd64

```console
$ docker pull clojure@sha256:f5d64a1040f589ce24e50e24628db6e23ebbf71044de35bd3cf1712b73e7bacb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.4 MB (287431577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:206bdf30c7ad276548b08e1aa955b684415b0ba6253f0968b2a63aad2c1bfd8d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c6b11972fd12973831818babf60f1ffc1c4047507943d132dffc612884022858`  
		Last Modified: Mon, 29 Sep 2025 23:34:14 GMT  
		Size: 48.5 MB (48480557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae240525ae2e6d39dc92e86908a0e8d8bc19cb6f221649395d23b16c6fa20951`  
		Last Modified: Wed, 01 Oct 2025 15:49:19 GMT  
		Size: 157.8 MB (157804776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e53d45200af21ed90ffe49f96d110ddb5cbd22c3a610590a821c2720f0b290a`  
		Last Modified: Tue, 30 Sep 2025 00:55:38 GMT  
		Size: 81.1 MB (81145204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cb1369c0267de7c7850ab3f964a8830daea9d6a0d97b2fc18ed61cda8ce9a61`  
		Last Modified: Tue, 30 Sep 2025 00:55:29 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:317951b3a0dcd87a624159e31697edc41a44467ba2f288407f23e596d7ee9efb`  
		Last Modified: Tue, 30 Sep 2025 00:55:29 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.3.1577` - unknown; unknown

```console
$ docker pull clojure@sha256:3d4c63d1194f4afc380492a0682e711a5ddb7d1c4aacd210f614716b2e24ed60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7395181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35677f04904a4fda2ef9dfbb18fc0eb29f9f9ad8a5cdb145317e071bb5f0faf5`

```dockerfile
```

-	Layers:
	-	`sha256:34c89b3c5d29462aa86183e8ece9de70007d873bd898c302691f541e1e22a36d`  
		Last Modified: Wed, 01 Oct 2025 15:39:53 GMT  
		Size: 7.4 MB (7378676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40580f4f16a8e441366190b71b693f4e677f5ac2c59fa8633f6b4e51faef10bc`  
		Last Modified: Wed, 01 Oct 2025 15:39:45 GMT  
		Size: 16.5 KB (16505 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.3.1577` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2cbba5df10adffdef261b3baeb843dd34a554c6f4ce989604b7ab528f4ecdb2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.5 MB (285469480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e2d97056ae19b7d2995047e6171f71dbc1ce3de9e01448576a6c47f83f027e7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f7b43f0d0a8b99591b27457b368e70a582002600d32503fd07798c1bee7cd134`  
		Last Modified: Mon, 29 Sep 2025 23:34:16 GMT  
		Size: 48.4 MB (48358915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9840c31b168bb172aeb5507c61f6c096f5577fc7590feb82e8e60a5cf8a2a72`  
		Last Modified: Tue, 30 Sep 2025 00:54:08 GMT  
		Size: 156.1 MB (156081234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db80cb1cd1c38694583a4ae10f58d11607fc7d88d9385ef43941732a0e9ff2e5`  
		Last Modified: Tue, 30 Sep 2025 00:54:28 GMT  
		Size: 81.0 MB (81028290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b3614bb55d398b0ccef344fc3488888091dbd3a5659e09674420dba1de9ea63`  
		Last Modified: Tue, 30 Sep 2025 00:54:21 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad56bfc20892f6f64e878ab5130647c61a866d168236965a64e71d165a2b436a`  
		Last Modified: Tue, 30 Sep 2025 00:54:21 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.3.1577` - unknown; unknown

```console
$ docker pull clojure@sha256:950b0ea8202bbc90d936d732987b31e4f50b6288de7b3911150af22cefee6e27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7401110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6065d6a040f5d7662ccb4195d030ed07826af37688187aee3493772849a28ed8`

```dockerfile
```

-	Layers:
	-	`sha256:5d471abe3460cb858cdaee1b9b173fa7733c81d546043dadec8291848d44b256`  
		Last Modified: Wed, 01 Oct 2025 21:41:38 GMT  
		Size: 7.4 MB (7384463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3faf5044daec2acafa71af5479a710221ad5ae7b47784a05c1136db53eb852cf`  
		Last Modified: Wed, 01 Oct 2025 21:41:39 GMT  
		Size: 16.6 KB (16647 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.3.1577` - linux; ppc64le

```console
$ docker pull clojure@sha256:6dac8798539bde022a40dfccecd1badcbeb39c0c4b6a70ecaa5f9698eceb4b51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297272127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbb4cae2cdc8ca6ddcfe91c06666bfad29ee68404c3479469c0702f92d64dda7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:812b25f785969d275d8c3962568c03f83ccc4df31b95f01c0646d79d6d5069f3`  
		Last Modified: Mon, 29 Sep 2025 23:33:30 GMT  
		Size: 52.3 MB (52326764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa4906f599b6daebf904dc5a7a8bdde204889076b4e24af0d5ff2121079af679`  
		Last Modified: Tue, 30 Sep 2025 06:16:03 GMT  
		Size: 158.0 MB (157963440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee65b27687f33f72776bfa9a1093d4e852f7ab76e6f5b480a07fde7a68a2a889`  
		Last Modified: Tue, 30 Sep 2025 06:19:37 GMT  
		Size: 87.0 MB (86980885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f0b0ee436c9644f4c317505a884f4f39f727477f1a727bcfcbb567859620b8`  
		Last Modified: Tue, 30 Sep 2025 06:19:32 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d45c10667fe2d4136bd19abb6687a355d2321ee09bc724189042e452dabff146`  
		Last Modified: Tue, 30 Sep 2025 06:19:32 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.3.1577` - unknown; unknown

```console
$ docker pull clojure@sha256:6092eb03f30d5befcd98326d7f2f524fe213729e51b6cd757313964c0815cf1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7400467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe02aa3afc845c19f8e56dd6b20dfdee8103681327eeef36d4d26b6efa3cfde2`

```dockerfile
```

-	Layers:
	-	`sha256:5f750b8fe8c3be14935aa87b6fa26eb355090df111aa25a567ee1b51633551eb`  
		Last Modified: Wed, 01 Oct 2025 21:41:44 GMT  
		Size: 7.4 MB (7383902 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a3421bd48618eddecfb2f2ac631d5333af679e825c4cb30a6d54a952365e195`  
		Last Modified: Wed, 01 Oct 2025 21:41:45 GMT  
		Size: 16.6 KB (16565 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.3.1577` - linux; s390x

```console
$ docker pull clojure@sha256:6cc97731920bef135e9cd2aa7bb8808a2ad36924f757e6eac7aa5b9fb2d48d82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.1 MB (274120976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4fdb14ce4a81c5d00f0d72ba46e90b81048237e186ddd8927757fb5df297c55`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:87d1bec83b35277b636c6e05b9418301b2f025752d7539cecae442f0b94d8fbe`  
		Last Modified: Mon, 29 Sep 2025 23:33:26 GMT  
		Size: 47.1 MB (47137446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6742edd5230b7019bfa83aae4e11ab81f1f9ab74f97e2d95fe82049a316cb54`  
		Last Modified: Tue, 30 Sep 2025 05:54:24 GMT  
		Size: 147.0 MB (147027032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17f8331714073320219a83c63c02b26328dd0c04259cee67f970ab76dcd5d76`  
		Last Modified: Tue, 30 Sep 2025 05:56:34 GMT  
		Size: 80.0 MB (79955460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2456e2f9cc8e14b72fb42e77bbc6149067e8ec263cac4a22da098ab307c11b9a`  
		Last Modified: Tue, 30 Sep 2025 05:56:30 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b013dcb409409d70673b6d1901b9fbd9be6545cb9961d5ee9380388f58af9f8a`  
		Last Modified: Tue, 30 Sep 2025 05:56:30 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.3.1577` - unknown; unknown

```console
$ docker pull clojure@sha256:b19cf4ff52f3fe4d523fbe9ba940a0b85c1bea668a084486cc2d8f448f70ac6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7386499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f20ac17722a6d6ec64cb3caa57661e8b132561d71535b826fbb1f7bf31b13ca3`

```dockerfile
```

-	Layers:
	-	`sha256:5926ed69e526c27e061bc2a0b376de357eeaa427ed8da89fdf9969486d060947`  
		Last Modified: Wed, 01 Oct 2025 21:41:50 GMT  
		Size: 7.4 MB (7369995 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2290deaa83cd003f3f878747cf352e1540bcef8d1260d684d25abd476cfb729d`  
		Last Modified: Wed, 01 Oct 2025 21:41:51 GMT  
		Size: 16.5 KB (16504 bytes)  
		MIME: application/vnd.in-toto+json
