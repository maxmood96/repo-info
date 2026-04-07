## `clojure:temurin-25-tools-deps-1.12.4.1618-bookworm`

```console
$ docker pull clojure@sha256:da01499d4a79417de0f5da38e6e546bf67cbdc6e080002a391a0ffb3b7f1eb0a
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

### `clojure:temurin-25-tools-deps-1.12.4.1618-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:a20a92885afd86695b1849e8cfb0163a5e60242c746d3c82a716be6029ee42ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.9 MB (221923921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbc1b6ee6f8b574592bcf5d7c7a1c3fe88c3ea6116ca8c34998958725c042a22`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 03:17:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:17:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:17:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:17:05 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 03:17:05 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:17:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 03:17:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 03:17:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 03:17:20 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 03:17:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c150dd3f5fc91eabd1818cc30298a4a956782621583cadfd369c4d327584008e`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.5 MB (48488823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afa56fe614695430ebf6dbaf5d33b5fabfb93494814f969b0012a87c3aff804d`  
		Last Modified: Tue, 07 Apr 2026 03:17:45 GMT  
		Size: 92.3 MB (92256298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c2c6eec1b159697cb930ba957caeeb7941ae08d28030de545b89def4c8b5d5`  
		Last Modified: Tue, 07 Apr 2026 03:17:45 GMT  
		Size: 81.2 MB (81177762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c8a27e28f21ef97790564e75d6eca9ba993225c664dd8b5611e9a5ca58790e`  
		Last Modified: Tue, 07 Apr 2026 03:17:41 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af6cf09ec3e3d6bc5db3301389f02c1b9a7a8994e3a35b342dbbd20a8222963`  
		Last Modified: Tue, 07 Apr 2026 03:17:41 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1618-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:47c27f5d356799df5a60a62409b28aa0c7439e8a674adcad775d20cd9d7c2f74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7365471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62686b6928944a9d43b318ffa63d565476d6447684a48735c36cd41bf296303d`

```dockerfile
```

-	Layers:
	-	`sha256:b1c05b0bf2695057c6e10acfc04954ca132ab51a78814f91232452f940a1d5db`  
		Last Modified: Tue, 07 Apr 2026 03:17:42 GMT  
		Size: 7.3 MB (7347700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45b0beca662c65ae8ca0bcd175f7e6ee05515b5394d3e21b10ddbf7e924491fc`  
		Last Modified: Tue, 07 Apr 2026 03:17:41 GMT  
		Size: 17.8 KB (17771 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.4.1618-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c904cfa4a2cb4fd93326c165b80fcba78038e678c38532841404a788d2b87d18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220821052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54281b990739cde81dc6bf24a36d095d71e5fe22ac2b2cf21000c6c08431292a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 03:28:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:28:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:28:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:28:01 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 03:28:01 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:28:17 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 03:28:17 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 03:28:17 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 03:28:17 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 03:28:17 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d03e31a3f7ef0d2866d799846c3a18286fab6fcddbd8c523f3cb5ed1bd2f31a3`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.4 MB (48373262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78d07c0a2b3ea68a2e73df43a2e01a5d7ac24c6101d398d9cf49237658a2f4b5`  
		Last Modified: Tue, 07 Apr 2026 03:28:40 GMT  
		Size: 91.3 MB (91288283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60917d6a521e9cf71ad41d3ceec0a002a94d83fa277692c0f3f851b97531739d`  
		Last Modified: Tue, 07 Apr 2026 03:28:39 GMT  
		Size: 81.2 MB (81158465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc107aa34e2912f396f00ff01e40512b79436d5f676c22263fefe133fff75f14`  
		Last Modified: Tue, 07 Apr 2026 03:28:36 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b2f1410944bc2cb8d36ed0d8b16aa3d3beb4109ae5235b6b3525dfa16f63a86`  
		Last Modified: Tue, 07 Apr 2026 03:28:36 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1618-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:8d493a433b9b20a9ee84f561b58cc4944eda72231734986fb2ed8d31be157459
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7371492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8281aa6e95b3fc4ed950919ae771b92710e33347cd1ea84ec2b23e902642a8aa`

```dockerfile
```

-	Layers:
	-	`sha256:26ad2bc1a40991faeccfd93f311ca8b3cfebe32eec75cc3761b158df7fabbba0`  
		Last Modified: Tue, 07 Apr 2026 03:28:36 GMT  
		Size: 7.4 MB (7353532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6cdb5d0238ef3d94e827f4dca00486a07011440c468fd4085008faddad4e9df`  
		Last Modified: Tue, 07 Apr 2026 03:28:36 GMT  
		Size: 18.0 KB (17960 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.4.1618-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:aa474b5618d6754a8095590f92c1fa2a8f84907c3025e8b4612f7d0c78e3273e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.0 MB (230970522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5634f2b6422339c13f5d5938c9b4db0e2afea2a2fb8e243ab61ecbdb2d289fec`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 18:03:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 18:03:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 18:03:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:03:56 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 18:03:56 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 18:48:05 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 18:48:06 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 18:48:06 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 18:48:06 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 18:48:06 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c072e92b832614e86d956c6381c6b7617944feae3193ea5691e9506870844136`  
		Last Modified: Mon, 16 Mar 2026 21:51:19 GMT  
		Size: 52.3 MB (52336698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81438db6b066b5319caf43fdad1d2cd4324d06132f04193db065dad00c8bc101`  
		Last Modified: Tue, 17 Mar 2026 18:06:02 GMT  
		Size: 91.6 MB (91632940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f167dbcba53acc80d6fd06080209eb579be2e3e166ec940ec6d1b922f4f84b`  
		Last Modified: Tue, 17 Mar 2026 18:48:46 GMT  
		Size: 87.0 MB (86999842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c7f948fcae1f290e78be61d0db05c77df181bf7a890966c63319c49e78cbd5`  
		Last Modified: Tue, 17 Mar 2026 18:48:44 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1302b136cdb8027be4c862b42c0f35ff66bfd8a5aecd76c3c75778e5c60ae7b5`  
		Last Modified: Tue, 17 Mar 2026 18:48:44 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1618-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:3b018df7759638fb6108a25df28b5a812f51647b7e17f292bfd0c4a15178212a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7354118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d394e2c2c20d4ed9e34618528e3124b8a5d0dca1f16925c0616cd094b9d99ba`

```dockerfile
```

-	Layers:
	-	`sha256:a8fbc374c6a0280bb2807ed0d3040ae8b06152c2b20407bbed6d7863357678fd`  
		Last Modified: Tue, 17 Mar 2026 18:48:44 GMT  
		Size: 7.3 MB (7336264 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4b7e8dfd598986ac85e931013e91e800bf73374a9b1414a8d7f278ca3c30861`  
		Last Modified: Tue, 17 Mar 2026 18:48:44 GMT  
		Size: 17.9 KB (17854 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.4.1618-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:3e790ca5dfef22f9954ad9c14b981b59cde1d79f39ed16ae79d5bae47f0f6d69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.4 MB (215371196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6ce0b11a546eace065a63bb0fefa7b10b16cbcb08c836bc15fd58a802f79932`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 05:38:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 05:38:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 05:38:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 05:38:40 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 05:38:40 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 05:47:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 05:47:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 05:47:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 05:47:54 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 05:47:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:40ecbf1d4e17f6b072e6cef463823baec601d9f21c9dc33d98bd258448a986f6`  
		Last Modified: Tue, 07 Apr 2026 00:10:32 GMT  
		Size: 47.1 MB (47148084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6336049cfea2fb1bf6fe937dfa06a3231de1bcd109cc0d07cc3ba41fd378402`  
		Last Modified: Tue, 07 Apr 2026 05:39:45 GMT  
		Size: 88.2 MB (88233804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19b094f534efd8875b5477a6fbceb9e28bf6c0aaf1f360120e57b42a374bd333`  
		Last Modified: Tue, 07 Apr 2026 05:48:20 GMT  
		Size: 80.0 MB (79988269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd93f4f66b08c3531a0b733e6d5d0b043c755b95ac93594bb90d5b1b3a091991`  
		Last Modified: Tue, 07 Apr 2026 05:48:18 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a4e31486c7492ded9784d6539d8cd4c90163a9f7c831ba535d83bc09d966b5`  
		Last Modified: Tue, 07 Apr 2026 05:48:18 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1618-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:46473c221197a049a7cf545472b649787b01bfb085b3394c75d3cf6c38d1ab78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7341352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68637d68b86e502b64513b03449da35429ae68fce94b19c4f3585bfd682c6d83`

```dockerfile
```

-	Layers:
	-	`sha256:c0cf42260a90b9c04c08951d623a01345d912da4f0132eb61808a282069b0d1f`  
		Last Modified: Tue, 07 Apr 2026 05:48:19 GMT  
		Size: 7.3 MB (7323581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b39cbadbe24091c5dbc8e92f4805ead7eaf94b04d8d3038f121d61dbacc8a8bf`  
		Last Modified: Tue, 07 Apr 2026 05:48:18 GMT  
		Size: 17.8 KB (17771 bytes)  
		MIME: application/vnd.in-toto+json
