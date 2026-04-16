## `clojure:temurin-21-tools-deps-1.12.4.1618-trixie-slim`

```console
$ docker pull clojure@sha256:9284796d0fb750fae32fe25fa85731e5fe9a317e2a20bfb62343ece9973150ca
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

### `clojure:temurin-21-tools-deps-1.12.4.1618-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:00031ca44f34fe71c5ba80966fe9ee437eff5e1c17993111574439f1459c4999
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.6 MB (262611184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f114186e1fe4015a8740cafc78dbd0ae63d82ad98a5cc7f193a99f3d63a78a6b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Wed, 15 Apr 2026 22:05:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:05:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:05:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:05:53 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:05:53 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:06:10 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:06:10 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:06:10 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:06:10 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:06:10 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2885dac90438a509e29959d4bd33fb5fe6fee467e6c62fbeeddabbcde52bb336`  
		Last Modified: Wed, 15 Apr 2026 22:06:33 GMT  
		Size: 157.9 MB (157857104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92382b862c58f85c8d32f56949c2d5da5de6738562378482dca0c338d1a4d273`  
		Last Modified: Wed, 15 Apr 2026 22:06:32 GMT  
		Size: 75.0 MB (74977397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4860450cc110e276716db01094f1e1b08fedbfa2612204fb52c079012021e343`  
		Last Modified: Wed, 15 Apr 2026 22:06:29 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c47aa80ff125510393032d10241b1fa13736e0cda6c085c273aebdfae0e50463`  
		Last Modified: Wed, 15 Apr 2026 22:06:29 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1618-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d9ce660652e122529541f5137e41a6adb83d621fdc2609f534f600d5327b9027
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5276802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24c8c5abf01d2eb4e988e105bcbf4f248703f9a6886cebe8ebf751c1249d17df`

```dockerfile
```

-	Layers:
	-	`sha256:df7f56342014ccf5014ffb5c2fb9c2e1fd0d8b30c64421d0a70489ea01d70157`  
		Last Modified: Wed, 15 Apr 2026 22:06:29 GMT  
		Size: 5.3 MB (5260990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f896d50f6cb1e3d0d1a00850cc2eadf9eb98313de8eab707a5390f239db1809`  
		Last Modified: Wed, 15 Apr 2026 22:06:29 GMT  
		Size: 15.8 KB (15812 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1618-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:aebb39eb711f2438dcacb0e3f56d7342bcbee023890f0571ea5a6f3068fb9c71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.4 MB (261422201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:067cce409dbd26662519946a01181ff186af2550eecb786c220959feb117c48b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Wed, 15 Apr 2026 21:52:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 21:52:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 21:52:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 21:52:39 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:17:23 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:17:42 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:17:43 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:17:43 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:17:43 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:17:43 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42232e8bb27cea0b0aaf7557129f3c3442ac8c57671a365e103e8938ec715aee`  
		Last Modified: Wed, 15 Apr 2026 21:53:50 GMT  
		Size: 156.1 MB (156133044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00786ba932eca9349d3cdc66bfe193703734f01a8d430836ba44f14b63602094`  
		Last Modified: Wed, 15 Apr 2026 22:18:04 GMT  
		Size: 75.1 MB (75149570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98f7e53346359dc3652e532d0420c35239f33d60b3003d4da6bfd3669aa1147`  
		Last Modified: Wed, 15 Apr 2026 22:18:02 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b8d5e1731edc1677b62c5b8d93c3d2f8d660b525004a5a6593222561e7bdf5e`  
		Last Modified: Wed, 15 Apr 2026 22:18:02 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1618-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:583b4bd15f6e32d772463a51d541c8d56cfaf41f62e54fb4914d23197652bd91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5281888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f64204ac513ad4ee117090a97ee717aa53dea5682c68e539523feae77b44b156`

```dockerfile
```

-	Layers:
	-	`sha256:7d67e57719de0ffb42342ada719be0bbd78eb0b221a4de9dcd9bca351d6df8d2`  
		Last Modified: Wed, 15 Apr 2026 22:18:02 GMT  
		Size: 5.3 MB (5266759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a379fe004afc28738312184177a9aea7958b5efec847972023af123f5953f30b`  
		Last Modified: Wed, 15 Apr 2026 22:18:02 GMT  
		Size: 15.1 KB (15129 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1618-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:33e4515bfb8d8d17e1faeb71b298d0a9f1435343df7d99136c8a4370dd2d4502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.0 MB (269000878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78f432a04864105f48e58ad2302d77fa21deb317b172e986e16048c15c4b9a90`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 14:48:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 14:48:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 14:48:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 14:48:08 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 14:48:09 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 14:53:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 14:53:40 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 14:53:41 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 14:53:41 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 14:53:41 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6e3428d4efac15fe7728b465c9c3bc5d71a07ad502becbd70250a2c560e32b53`  
		Last Modified: Tue, 07 Apr 2026 00:12:50 GMT  
		Size: 33.6 MB (33593016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aba66074989fc6e37b18a04cc78cb4c1a09ae249fb0aea194ade5c8d6049e645`  
		Last Modified: Tue, 07 Apr 2026 14:49:29 GMT  
		Size: 158.0 MB (157977472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73dd48215e552ce3e95aa0c3e88c1214f30d9d412850f30573de6db7f32719cb`  
		Last Modified: Tue, 07 Apr 2026 14:54:17 GMT  
		Size: 77.4 MB (77429352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:857f8c02eb2c59dd99cd382527d685febd3c4bd5d0e7532afb65b89e16567357`  
		Last Modified: Tue, 07 Apr 2026 14:54:15 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e4d96f35a3b5ae933046795b4d85596f451b53b3d18b262c46211cbd11bfb83`  
		Last Modified: Tue, 07 Apr 2026 14:54:15 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1618-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:fcf832372d1bfa4596e1e874b8b34be7a0d8b606670af7a7ae2b3d5bd18c0cee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5281221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe3498b1508d676f6d5b09437df8f423dfc8fc0bcfdb4c057d3a25e50e6e1493`

```dockerfile
```

-	Layers:
	-	`sha256:c3817a5afa777c8bf75fbbe54a50e3fffb6812d2e2f5adb526fee85f9754a2a7`  
		Last Modified: Tue, 07 Apr 2026 14:54:15 GMT  
		Size: 5.3 MB (5265361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34ac09b53b67bf33a6c7ce1589ea9efac19c1c46a8ea0620b6d17f56c0cfa43c`  
		Last Modified: Tue, 07 Apr 2026 14:54:15 GMT  
		Size: 15.9 KB (15860 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1618-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:f8d5d9d26d5c1f5e3fbdf788300550c30e9db41dc6b79614124e638e31cd0b93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.0 MB (259013063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0d04249c33eb4adc4985f567b267db1cd161ac276e54cbaa26d72fb878e0b21`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1775433600'
# Sat, 11 Apr 2026 22:00:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 11 Apr 2026 22:00:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 11 Apr 2026 22:00:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 11 Apr 2026 22:00:57 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Sat, 11 Apr 2026 22:00:57 GMT
WORKDIR /tmp
# Sat, 11 Apr 2026 22:24:51 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 11 Apr 2026 22:24:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 11 Apr 2026 22:24:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 11 Apr 2026 22:24:52 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 11 Apr 2026 22:24:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:51128e253868f85aa5e3b9e86448414d946e8a6b685e02db1030aaa2b11e81d4`  
		Last Modified: Tue, 07 Apr 2026 01:55:37 GMT  
		Size: 28.3 MB (28275778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5427f8f7357cd1c2f90f35451416b331ea3c682f95a93bd8689b142ddc99805`  
		Last Modified: Sat, 11 Apr 2026 22:07:07 GMT  
		Size: 157.2 MB (157216895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a6346c48e4f379f3ec3b83122c30dad50bbdefaaded89900864456e11458b45`  
		Last Modified: Sat, 11 Apr 2026 22:28:39 GMT  
		Size: 73.5 MB (73519344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffc56979dd81f7a5d64765eaab6c670746cec1d8ad6cf84f6767ca200583f22f`  
		Last Modified: Sat, 11 Apr 2026 22:28:28 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a12d4e061a5a92a94c0db68b4c0263c74d9e24ed9d56c599c7b2d770fecba2ce`  
		Last Modified: Sat, 11 Apr 2026 22:28:28 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1618-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7a675b8363be8f55a4b92a096c911e84647ab5ba5c9443c63ed5909da454414e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5266312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65846ea359501492a6a5dc6a9547c576dfc1464c5a9a251319e3dd9602bc9104`

```dockerfile
```

-	Layers:
	-	`sha256:91643b64ba53d7af815a76506d42568dd84ffa663aafb0c07b215dcbe473c495`  
		Last Modified: Sat, 11 Apr 2026 22:28:30 GMT  
		Size: 5.3 MB (5250454 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e61613f591d1f8a794b2c362392a27f212dd5f57be757e6f2ec02a53f60c5bab`  
		Last Modified: Sat, 11 Apr 2026 22:28:28 GMT  
		Size: 15.9 KB (15858 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1618-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:52ba36cc5236fcfbe8df82c2ae03d5d5fda78a802416f3957622ba9738608021
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.5 MB (252540260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:723ddd7f0c592425a484cf00a1a608cef767ff723d8928cc4061274752cb3f9c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Thu, 16 Apr 2026 00:41:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 00:41:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 00:41:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 00:41:51 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 16 Apr 2026 00:41:51 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 00:43:19 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 16 Apr 2026 00:43:19 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 16 Apr 2026 00:43:19 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 16 Apr 2026 00:43:19 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 16 Apr 2026 00:43:19 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:82e48a38ec87473a03164a244b5d8dfc2b55ef7a891305e41ee39d937de3c4a4`  
		Last Modified: Tue, 07 Apr 2026 00:13:47 GMT  
		Size: 29.8 MB (29835418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dcda4ee8bd621aac2ef8027b80495558658cc850eca58d63e93743bca8b01b4`  
		Last Modified: Thu, 16 Apr 2026 00:42:33 GMT  
		Size: 147.1 MB (147105251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07e97b5ac60e80fa6914b0b0d53fa4d2e8eea4eebac818afe7e383010306e40`  
		Last Modified: Thu, 16 Apr 2026 00:43:43 GMT  
		Size: 75.6 MB (75598549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a928ecfbb6d351d813a5b226036f14229d0424ead99ebb83a83070aa404b55`  
		Last Modified: Thu, 16 Apr 2026 00:43:41 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57078e2cab2d2894567179d961edacc2fbdbaeb24095cb2b7cffaeb1d3094b83`  
		Last Modified: Thu, 16 Apr 2026 00:43:41 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1618-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:01cb671e4d7870de262c0cd35347cd0c8629c08dc927b50ddf922267d6899d6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5272726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39c5f393c75511586cc925b84a3e1785a8d673fd6f3b33ea0041d8c2c8ebc77f`

```dockerfile
```

-	Layers:
	-	`sha256:122844a4fa6911d9e102a96e4216bc8b4fea900dab43859a2b660a836654ea13`  
		Last Modified: Thu, 16 Apr 2026 00:43:41 GMT  
		Size: 5.3 MB (5256914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cd3fec23fafb919d2372e0ecb10e9f2efeb1563d9f7c386742b46d7354bbca2`  
		Last Modified: Thu, 16 Apr 2026 00:43:41 GMT  
		Size: 15.8 KB (15812 bytes)  
		MIME: application/vnd.in-toto+json
