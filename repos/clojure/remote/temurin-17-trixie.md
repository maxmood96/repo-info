## `clojure:temurin-17-trixie`

```console
$ docker pull clojure@sha256:58074902f9cca7b3eecbf874fd463ec13dc2c5ba4e570b3ecb8c6055b4b8d583
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-17-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:c4e3c1626bdf7a565e9243e1965901b668ed22ecb6b4674051781507b5c46fd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.8 MB (280779586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e32c6b6e1a89e40b863e1dbf40c0f8bcb8cd5f52a943022b317364c03bd8f959`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Fri, 08 May 2026 00:08:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:08:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:08:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:08:04 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 00:08:04 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:08:21 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 00:08:21 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 00:08:21 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:08:21 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:08:21 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3b32e3bb7338c216b077e95920ae53332d81bd57f4a7393bc324432d5a3f88a2`  
		Last Modified: Wed, 22 Apr 2026 00:16:56 GMT  
		Size: 49.3 MB (49302102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45f0895b04c2c726579914f7b3db98583bf61ac00d926f77c8e89ee54fe408bf`  
		Last Modified: Fri, 08 May 2026 00:09:02 GMT  
		Size: 145.9 MB (145905473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f20977bbb3b5f4ecff74ad51265b88081f8b554d9688a30b5ecb83fd1ad10c`  
		Last Modified: Fri, 08 May 2026 00:08:41 GMT  
		Size: 85.6 MB (85570970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f8d795f2700d2247f68202ba41145fd99c5e6b21fc80008c07f5d76eb59b168`  
		Last Modified: Fri, 08 May 2026 00:08:39 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:245ad3da80138b6a3b240a177c69aa4c4b818811e1e5a6408b6debf3b840257f`  
		Last Modified: Fri, 08 May 2026 00:08:39 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:fe17a463d749b14d1dcd63abbb072e66fa03be300d7dba6c12e8416a5e65f436
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7487256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb29db59d43b0deaf863ccb67da96b8aa21b425302e2e30e779c45c0a8f3d0c3`

```dockerfile
```

-	Layers:
	-	`sha256:2c2dfee2a7fefec167b1bb6b2ce37fab00a1544ba631623b364ac41593757760`  
		Last Modified: Fri, 08 May 2026 00:08:39 GMT  
		Size: 7.5 MB (7471348 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1858a6f7346b65ffede912f7e6b9d5ac8ca8c0c25a4135ca22d5708106b9c646`  
		Last Modified: Fri, 08 May 2026 00:08:39 GMT  
		Size: 15.9 KB (15908 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d60a6306eb3e64163498dd78d1885a557c8018feee1b0223eba8cfe55924356a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.8 MB (279778006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a6c13e0eeb849464cecf6f01b545d39815cddd9b1b72dacbf757b0dfa257e78`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Fri, 08 May 2026 00:09:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:09:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:09:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:09:58 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 00:09:59 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:10:15 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 00:10:15 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 00:10:15 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:10:15 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:10:15 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6e7932d5cb5573d1bff4fb8801baad19fc72d2ae741bb046333573653944f5a5`  
		Last Modified: Wed, 22 Apr 2026 00:16:45 GMT  
		Size: 49.7 MB (49669245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18e54db7456e1f715b4bf3be4e072e5a403505f7652991418eb435c432069495`  
		Last Modified: Fri, 08 May 2026 00:10:37 GMT  
		Size: 144.7 MB (144724334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eff8e471386030c472570d33119321b985ec8866801ca543bd6b52b6cd73127`  
		Last Modified: Fri, 08 May 2026 00:10:44 GMT  
		Size: 85.4 MB (85383389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33d66bac59f2c32a43f3ebfe3314bd39a17a5753f73641d07b7adc7250b2799e`  
		Last Modified: Fri, 08 May 2026 00:10:33 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62231c6e3899142d8bec5d6b63661edd63592a462573b5b9402363fc9834ef4`  
		Last Modified: Fri, 08 May 2026 00:10:33 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:ff405ad39feb528addb89c5c0e44284547fd18e7a00cc4969f1f146fa5558a80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7494404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1964136b6c5b145c5cb2b67f22a3e42b362441f40fbc3594a76662b265ce54ab`

```dockerfile
```

-	Layers:
	-	`sha256:8d62497ce049ee30f560114a87e3a3659f291fa82530d158dd3bd0f3fee57ba1`  
		Last Modified: Fri, 08 May 2026 00:10:34 GMT  
		Size: 7.5 MB (7478378 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57d729817465e904626523c0c83ddef00710acbc2bbff02a8812a2fdd0400cd6`  
		Last Modified: Fri, 08 May 2026 00:10:33 GMT  
		Size: 16.0 KB (16026 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:be12f2ee0b1d4d74c40fc85c48efb5c00cbfed3d4e024c680ba708490603771e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.9 MB (289876768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fc2531f2004aa97091963b9177c3bb035761fa2bb08679684740ea3b85dd937`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Fri, 08 May 2026 00:45:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:45:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:45:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:45:58 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 00:45:59 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:53:15 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 00:53:16 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 00:53:16 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:53:16 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:53:16 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0fab4f6170940889900b2327e1b3c62dace993eab8074ca7d33d1ffeef137c08`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 53.1 MB (53122984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:937b7eb5aea1a56bc2fcf2ec92c34b7b899cf187331f6afa218be284e921541e`  
		Last Modified: Fri, 08 May 2026 00:47:15 GMT  
		Size: 145.8 MB (145766229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:669bd8c7c869f8fb3755cbf26d6676b40596ba3320dbd286d8f4279a611e7644`  
		Last Modified: Fri, 08 May 2026 00:53:56 GMT  
		Size: 91.0 MB (90986515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f7e6365702509ead0cc28131f0cafc6b909c175ea52e9ada76a8f1237f1a7e`  
		Last Modified: Fri, 08 May 2026 00:53:51 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df182d32e5646108ff40e0cd71cdd6d04ac8797b182504c8f4c63e6e47d8039`  
		Last Modified: Fri, 08 May 2026 00:53:51 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:fd217bba69c7dfc436ca1310f2f112e7b7f791ff88b8dec3b697021e87792428
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7491724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3f041abd609de7fdcec916726d1860b4a6df69e8834d358d8204cf7fe770bd1`

```dockerfile
```

-	Layers:
	-	`sha256:e56c1a3a49ce0e6ada4607c10a2d48b311ea239e9be7ba0599a4ca2b06ed299c`  
		Last Modified: Fri, 08 May 2026 00:53:54 GMT  
		Size: 7.5 MB (7475769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3287daab11ec68bfff43bc1ffdaa01ad986dcd147b5be5694d933e5f35edd1d`  
		Last Modified: Fri, 08 May 2026 00:53:54 GMT  
		Size: 16.0 KB (15955 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:5f77804697060f1c518ca7733d34f110dad97e3e4520b6a1ef4e92a4b9ef4b67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.9 MB (274921312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a966d011554534d39f899f928737ef152c44b22e67c7cfaccc6b192d2432a447`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Fri, 24 Apr 2026 17:41:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 24 Apr 2026 17:41:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 24 Apr 2026 17:41:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 Apr 2026 17:41:31 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 24 Apr 2026 17:41:32 GMT
WORKDIR /tmp
# Fri, 24 Apr 2026 17:57:17 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 24 Apr 2026 17:57:17 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 24 Apr 2026 17:57:17 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 24 Apr 2026 17:57:17 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 24 Apr 2026 17:57:17 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6e518626ae0de2d990c7c66185d308a25cb3affebb6204543438f56fd9f94992`  
		Last Modified: Wed, 22 Apr 2026 02:29:17 GMT  
		Size: 47.8 MB (47798217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca059398ab85ec46154b4adc01fde7c5c787818bd1a043bdd89c080ecbd2e3db`  
		Last Modified: Fri, 24 Apr 2026 17:47:36 GMT  
		Size: 142.7 MB (142662892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bafc3d45da4972b3524556b66cc3571fb9129ecf9fbfc391a903a4d428cfabc1`  
		Last Modified: Fri, 24 Apr 2026 18:01:48 GMT  
		Size: 84.5 MB (84459162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d032f5acb1f07b3532d695c592bea544200b56fb76a4adabb87d2224d820aea0`  
		Last Modified: Fri, 24 Apr 2026 18:01:35 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc17400ed1407e8d15ef31946f0851e3c8d37fdeb01cb09503f9eb60660770d`  
		Last Modified: Fri, 24 Apr 2026 18:01:35 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:4d996b2878cb60199394c2c2086b42dc7677a2617625dd86834400922e449584
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7472518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5487c01c76cd2fb12f6e78d2b96bf113573d7a31b8ab2df106449e810fd7d087`

```dockerfile
```

-	Layers:
	-	`sha256:54b4470a90a5042c4fcd6127654c711015e87c4d98de367b1b26647d9c3e7e4a`  
		Last Modified: Fri, 24 Apr 2026 18:01:37 GMT  
		Size: 7.5 MB (7456717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6553cdd66f9ae918428a7e3d437d877e9cf2400e081afbd90e64ae11fc7f6d9c`  
		Last Modified: Fri, 24 Apr 2026 18:01:35 GMT  
		Size: 15.8 KB (15801 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:a2ce3ac3a773f5d1f56bf4becae6c7e594c16dbd355a093e2ad548493f901d3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.5 MB (271545507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23b0bb63bfbc746a4745ecef005b63c5c75658f902e5408a604ab74824aaf9bf`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 04:02:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 04:02:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 04:02:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 04:02:08 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 04:02:08 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 04:02:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 04:02:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 04:02:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 04:02:26 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 04:02:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:943402c24d6e7299016c00f751297dfb5fc1821547fdd1d9c56a206079784185`  
		Last Modified: Wed, 22 Apr 2026 00:17:09 GMT  
		Size: 49.4 MB (49372106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56bdf2a5fa643efe0a338a41632a93331b8ef5e9ff59f12ff100e1acc79a8c48`  
		Last Modified: Wed, 22 Apr 2026 04:02:58 GMT  
		Size: 135.6 MB (135627001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f0d160a298654cdb60a8dce3d117a776855c9233be01e89c4b5dc68eaeb317`  
		Last Modified: Wed, 22 Apr 2026 04:02:57 GMT  
		Size: 86.5 MB (86545358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ac60a56f4dd90208d6c5ed19124485e5e5ed3bc4bc12ae77557e09175a27a7a`  
		Last Modified: Wed, 22 Apr 2026 04:02:54 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9764f978077b5eae2193478b3e02004c48f4fe581643b257398b92339ef534c5`  
		Last Modified: Wed, 22 Apr 2026 04:02:54 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:9a5ce71978b41cbaf0ba309e2df4c5b4f11197b4bf96c48175c93b0d1a3dbee7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7482397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70d38c336906c63265228a65f7c0a51e789fcc21e53b7b04400fa71fd5a056d6`

```dockerfile
```

-	Layers:
	-	`sha256:d6645f2703e665e2aa269c282c4b961d4b1b109557af72b24c40fd71df13e45e`  
		Last Modified: Wed, 22 Apr 2026 04:02:55 GMT  
		Size: 7.5 MB (7466643 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f30728161dff114bec41e7a9011b0b9c4897dbb6a3c1a38e30b774de2aee3088`  
		Last Modified: Wed, 22 Apr 2026 04:02:55 GMT  
		Size: 15.8 KB (15754 bytes)  
		MIME: application/vnd.in-toto+json
