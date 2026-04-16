## `clojure:temurin-21-trixie-slim`

```console
$ docker pull clojure@sha256:ae37a8b394c086bdf5d8c9a837c9003022dc9882bc2cf3432c44bd2737719b11
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

### `clojure:temurin-21-trixie-slim` - linux; amd64

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

### `clojure:temurin-21-trixie-slim` - unknown; unknown

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

### `clojure:temurin-21-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5ac03d6c7c10bc648cc15705b0acea97adb963fd04dc4aa1b7b13c5028ca205b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.1 MB (258104369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88f503d46fdaaa0155e41e6b66b184635a46a24fb7ff26ba19d4c6b59300bcb7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 03:26:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:26:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:26:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:26:33 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 03:26:33 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:27:47 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 03:27:47 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 03:27:47 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 03:27:47 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 03:27:47 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c1c3a34ef57280cf5c0e533c81d90c0e60f26075860ec24985d325b0935a93`  
		Last Modified: Tue, 07 Apr 2026 03:27:14 GMT  
		Size: 156.1 MB (156133064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edce20d072a55d0da79d1af7d9151a4e4ebdc464a4540215919526619f9d6307`  
		Last Modified: Tue, 07 Apr 2026 03:28:05 GMT  
		Size: 71.8 MB (71831713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:836a84aa1a28b3e7f099e18382a3d190c72107f5098a479ac3ed611b1121ba53`  
		Last Modified: Tue, 07 Apr 2026 03:28:04 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5216e9d3d6c71f610b831a2f8f63e01adbdf560405924c119a92ed3ccbd8cea6`  
		Last Modified: Tue, 07 Apr 2026 03:28:03 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:943db2f75c3b85d655e5be53e9b17e44654c76eaa40fbbbce3d6b1e0c8fbe8a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5282689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7735fb1a1e95dd825ae46a9afdb845ce8356c38abf603e6095421c878ba3c3fc`

```dockerfile
```

-	Layers:
	-	`sha256:da0add43b028712a2032551c57473f3205d7acc36fca81890852b927d37673e9`  
		Last Modified: Tue, 07 Apr 2026 03:28:04 GMT  
		Size: 5.3 MB (5266759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48d4ba7ff55f2b6782cfc037ce5bf28662ca67e0d51f1172c011e5916eeaa2da`  
		Last Modified: Tue, 07 Apr 2026 03:28:03 GMT  
		Size: 15.9 KB (15930 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie-slim` - linux; ppc64le

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

### `clojure:temurin-21-trixie-slim` - unknown; unknown

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

### `clojure:temurin-21-trixie-slim` - linux; riscv64

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

### `clojure:temurin-21-trixie-slim` - unknown; unknown

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

### `clojure:temurin-21-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:10aebca408a5add621327f424ead0918cce9c45ef180115973197549da07064e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.9 MB (249928731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83a9779daee88a35a6b66086f9a3fb4be80a573b9cb90f18f9153d5a70dc81cf`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 05:46:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 05:46:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 05:46:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 05:46:26 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 05:46:26 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 05:46:43 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 05:46:43 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 05:46:43 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 05:46:43 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 05:46:43 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:82e48a38ec87473a03164a244b5d8dfc2b55ef7a891305e41ee39d937de3c4a4`  
		Last Modified: Tue, 07 Apr 2026 00:13:47 GMT  
		Size: 29.8 MB (29835418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32bc4ccf718b91e6d661df12976987fde0beff316e149a5b77a4424557d38ee9`  
		Last Modified: Tue, 07 Apr 2026 05:47:13 GMT  
		Size: 147.1 MB (147105211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9d582f7becf81eda9951c35ed284b91860a9627e639a0d54d079165824ad6e9`  
		Last Modified: Tue, 07 Apr 2026 05:47:12 GMT  
		Size: 73.0 MB (72987061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e7b4a14c675c6afa039233a00779cf69b5f9a4fcc863dd392a9f690c9849202`  
		Last Modified: Tue, 07 Apr 2026 05:47:10 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ca9c429f539c03b5bda01ddc7ab7707fa44fce5af09a4cf45e738b81ce84ce4`  
		Last Modified: Tue, 07 Apr 2026 05:47:10 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1f428b13108c44a212c2aedf63a31a856d7030d4ba75458afcf44f3cbdff5441
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5272726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10c59ad1df71fbf40e4472ce65785d7571e2a7316bc9111a11a73d84ee8e0888`

```dockerfile
```

-	Layers:
	-	`sha256:648f6325b11d9021374597249a6b23b77f66feb3a493af7ce817c85555398663`  
		Last Modified: Tue, 07 Apr 2026 05:47:10 GMT  
		Size: 5.3 MB (5256914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09f0fd9b70f4972232a6fcccf9c5e2c023bb2084df3a0155956aca32549d1919`  
		Last Modified: Tue, 07 Apr 2026 05:47:10 GMT  
		Size: 15.8 KB (15812 bytes)  
		MIME: application/vnd.in-toto+json
