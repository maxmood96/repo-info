## `clojure:temurin-26-tools-deps`

```console
$ docker pull clojure@sha256:5d66572bac40d9a06e0abc389f7c562de0fd25d78147232c0709336adc022ea1
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

### `clojure:temurin-26-tools-deps` - linux; amd64

```console
$ docker pull clojure@sha256:0280223abb5b672f12022c22bb09a7b7616b28ee076230068bb9bb175b868288
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.2 MB (224158764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3b7ebb4ffcf21943cc2e88035ef8a30758929812365516de39095046740ca0a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Thu, 14 May 2026 23:36:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:36:47 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:36:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:36:47 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:36:47 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:37:02 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:37:02 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:37:02 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:37:02 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:37:02 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9104793a826a01456b0ba567a92064e85a029816661fbb4524da7913f0123ab5`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 48.5 MB (48488676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35f1cefac79e4aca1278deed574b5aae205490ea61839de682702bab8bb681b8`  
		Last Modified: Thu, 14 May 2026 23:37:24 GMT  
		Size: 94.5 MB (94455681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc9ee6922881875c825df976221550672f48688f26eed4650fce528e77852a4c`  
		Last Modified: Thu, 14 May 2026 23:37:24 GMT  
		Size: 81.2 MB (81213363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b41678e04c292e683a2ad6951c1742f05ff9b07c627029e18d9dbceee6897fa`  
		Last Modified: Thu, 14 May 2026 23:37:20 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a28a4c55e8663e02075dcf240427fdfaa9e33b747181f343ee3bb68ce8d94f3c`  
		Last Modified: Thu, 14 May 2026 23:37:20 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:80310955c89d8ba5cafa5ca5134dcf39cbbe0b4a37220eb40654678514f64945
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7360943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2171c82e9d03bdf8f179a11e9bc1c58848bc127a58993211288e859cacb931a`

```dockerfile
```

-	Layers:
	-	`sha256:094f276e2fdaf8baa45d11174173b66bcdc1c04fa43aed3592b329c356514445`  
		Last Modified: Thu, 14 May 2026 23:37:20 GMT  
		Size: 7.3 MB (7344488 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:943028b1e8b5473490f9f3bef8d997f6c11739f2734b64b1ac0d69804f24c8fa`  
		Last Modified: Thu, 14 May 2026 23:37:20 GMT  
		Size: 16.5 KB (16455 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0925d44fc201717f38f5f273027f91201d9cb07b2996f06d89136c1d937bb1f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.0 MB (222965210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61e63afe2ccd28f8a7665b0ce53a022b214efadd971ead69475eee73edd3ee06`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Thu, 14 May 2026 23:36:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:36:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:36:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:36:57 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:36:57 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:37:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:37:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:37:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:37:12 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:37:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8eda28c6ece628fdff982fd6c7c1cd1f5eeccc51cfd0a3ee9155b2ccbdcc68a3`  
		Last Modified: Fri, 08 May 2026 18:24:51 GMT  
		Size: 48.4 MB (48373150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16e5b80348ec66e612a7091f2e45aeab928c75f4fbd12411de21d9a611e12ed`  
		Last Modified: Thu, 14 May 2026 23:37:34 GMT  
		Size: 93.4 MB (93395165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30098ce5ad520a30c3d3c4cadf7b9616577dd3cf8175a1c9fd2c0fcfc7fdd1df`  
		Last Modified: Thu, 14 May 2026 23:37:34 GMT  
		Size: 81.2 MB (81195853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aea8d9b5562c4a1f12cbcce85863f32f7f96686616968a9b70adda58430e526`  
		Last Modified: Thu, 14 May 2026 23:37:31 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918f2831af564aa39d246b2da31ca568f964f6e13d703329068c183f703e1ba4`  
		Last Modified: Thu, 14 May 2026 23:37:31 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:f95627543394b6aa352e1377326ea2f8be74117749f947e0b11c3f460844963a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7366867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c02f83a8b71127c737e9a199f36dc4ebc284492907a96e066765721571cf0c09`

```dockerfile
```

-	Layers:
	-	`sha256:2ee72ad8e1097d5e1cbf7e453fe6791d19737ffd817a559a356f2dc11efe491f`  
		Last Modified: Thu, 14 May 2026 23:37:31 GMT  
		Size: 7.4 MB (7350272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20881b2023fe9a426d2efac7bcaf2589345e4aca10e1b60cd07394b5e6aa3635`  
		Last Modified: Thu, 14 May 2026 23:37:31 GMT  
		Size: 16.6 KB (16595 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps` - linux; ppc64le

```console
$ docker pull clojure@sha256:3ec14729f55f58d5b1c30f06fe741584294be7fa5045c0d7369542f022feb2b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233153062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1b92298154de370d504a05233e2cae14428ebd67b2da2b9c73407b615e8ce79`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1777939200'
# Sat, 09 May 2026 02:46:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 09 May 2026 02:46:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 09 May 2026 02:46:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 May 2026 02:46:54 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Sat, 09 May 2026 02:46:54 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:56:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:56:31 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:56:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:56:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:56:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:30ef9f53c997c6c1f1ab8f4cc559b32d9206d169c54ad5a0f0363076708fffef`  
		Last Modified: Fri, 08 May 2026 19:44:07 GMT  
		Size: 52.3 MB (52336787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c82bc18c543cfc7a609b53543d15f2cb535420968abe79adcd8cc8351b5f32b`  
		Last Modified: Sat, 09 May 2026 02:47:58 GMT  
		Size: 93.8 MB (93781452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57055ab4068804a255000a1d8f8137604f6764728b5e4bbc440bafc9922815ab`  
		Last Modified: Thu, 14 May 2026 23:57:17 GMT  
		Size: 87.0 MB (87033777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d692866d46ee30df3fd3c38ccf0d7947affcea3b4098357b6cd3e3b8be57066b`  
		Last Modified: Thu, 14 May 2026 23:57:14 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afece31d809ac000f09dc07ab14b0529d9a3c4160cb201ca0e7d0d8a8ac41e1f`  
		Last Modified: Thu, 14 May 2026 23:57:14 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:a29b54ea9eb3708524b0a60acfa7b32a84c9150ec80c67257d6a0f6cd27379bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7350167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4cd6a7421c596bafdcc3ca71c3b7395828e6da20660f795dc8c9f0a87ba4c88`

```dockerfile
```

-	Layers:
	-	`sha256:d69f0fb779106b5157abe8f5b3641202d0f9b47a455351764da8a2dd60507e61`  
		Last Modified: Thu, 14 May 2026 23:57:14 GMT  
		Size: 7.3 MB (7333652 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b27f57ba72d6417f8d605a6f70e5b477406b70f5ff91c3041b12985b0b64fadb`  
		Last Modified: Thu, 14 May 2026 23:57:14 GMT  
		Size: 16.5 KB (16515 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps` - linux; s390x

```console
$ docker pull clojure@sha256:d47f4a9acc965771a6d9b94276bab14a3af48b9cc9a630e4776aed9abf8b5749
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.7 MB (217721505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d50e0bcefe284512caaf4d04f0e88a56dcde69140b4e1ed5e36e7efc6a1cab7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1777939200'
# Thu, 14 May 2026 23:38:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:38:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:38:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:38:50 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:38:50 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:39:02 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:39:02 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:39:02 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:39:02 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:39:02 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:124dbe049873037f973f01d877ec004bf4cd3ce5723d0b8f2067c58ad98137d6`  
		Last Modified: Fri, 08 May 2026 18:27:29 GMT  
		Size: 47.1 MB (47148023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac890030073063cf5445628a264498a134bda1d642b67c0abde24149e83bd386`  
		Last Modified: Thu, 14 May 2026 23:39:31 GMT  
		Size: 90.5 MB (90547678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daf1926788a5a12b825ad4cb0d545e3fd00ed460f8716219fcaa416de5b6cb72`  
		Last Modified: Thu, 14 May 2026 23:39:31 GMT  
		Size: 80.0 MB (80024763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:135ca2f2d66846ccce8ef97e8b076915a90e55ebecd6c62b8df3053ead27f4e2`  
		Last Modified: Thu, 14 May 2026 23:39:29 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e87afa44a51d1a68f5e39e36858e5df2221981fda67f5c29f159dd9aa3d7589`  
		Last Modified: Thu, 14 May 2026 23:39:29 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:c3e4eb8e73223356a50e298f83a89def3fda84730a8d82b09795e988bd3b8a22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7337448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:727f56864b8a5b7217490a084737bbeeecbdec672a6c9587c2aaf0592a502678`

```dockerfile
```

-	Layers:
	-	`sha256:b31223e009904b7e20c62e08486a3c4c4234b896d138b0ca5a12523ef0d6b277`  
		Last Modified: Thu, 14 May 2026 23:39:29 GMT  
		Size: 7.3 MB (7320993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5f16570d6d970d477b487d30a2f2b7f1cab8977c5d65f4c29fd02eacb163bc5`  
		Last Modified: Thu, 14 May 2026 23:39:29 GMT  
		Size: 16.5 KB (16455 bytes)  
		MIME: application/vnd.in-toto+json
