## `clojure:temurin-25-bookworm-slim`

```console
$ docker pull clojure@sha256:d64e794f0cfcb29ccb399b6ab4a5fff7c91d02e33d6bf9b52b41c21d02d35c09
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

### `clojure:temurin-25-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:f69560ad796b977b4254fdf4a79e4ab62cea660521ac106d98063fe06ec0593d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.2 MB (190192799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f04036fa3998752285e97c6e5e4e7c4b1860205601972f51e28c08be10ad5bbd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Wed, 15 Apr 2026 22:06:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:06:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:06:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:06:43 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:06:43 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:06:57 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:06:57 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:06:57 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:06:57 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:06:57 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:da539b6761059a0a114c6671f1267b57445e3a54da023db5c28be019e40f0284`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.2 MB (28236332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e37cc7d902a86c38ce1e23e9c33f70d245f7c5e842c46b908b301874ed87b19`  
		Last Modified: Wed, 15 Apr 2026 22:07:19 GMT  
		Size: 92.3 MB (92256337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd36792dc864c950aa7fe81fa0d52135b2c7944982fe1d86a1da8eea5b836dbd`  
		Last Modified: Wed, 15 Apr 2026 22:07:18 GMT  
		Size: 69.7 MB (69699086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4279beb899d705995252e6273169d9fab87da7daa02982b0c095f3abe3f6c6cb`  
		Last Modified: Wed, 15 Apr 2026 22:07:15 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b519771eb9288b37717cf8109b28ecb63ea7b014fe4674c69cd5edbac1b9707`  
		Last Modified: Wed, 15 Apr 2026 22:07:15 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:fa4d7b95a1126815b05695b4139c75bfa7c8ce916660b5365f25d8c8426f6fd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5100786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eec65e4898a9161abdbaceb511e4188b7eb25b87d494a79b53e2585b5cbe6a76`

```dockerfile
```

-	Layers:
	-	`sha256:ccc4ee1ee94b74b26db80b57d4c038fcd4ee00b14c9f4db259d0809d39f1ac8f`  
		Last Modified: Wed, 15 Apr 2026 22:07:15 GMT  
		Size: 5.1 MB (5084261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1df2f298726d5430aa770886fb8ff3686139327ba58a2444951015f747940aa`  
		Last Modified: Wed, 15 Apr 2026 22:07:14 GMT  
		Size: 16.5 KB (16525 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7dad99b64d4fc6b6ebd07eb18191280fc20b7d4a4c8802287cfee75face53344
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.1 MB (189094450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:185d598a323f7b7c7feac1525523e5bfd699ad674ff837895f14a4b74523e8f7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 03:28:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:28:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:28:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:28:05 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 03:28:05 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:28:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 03:28:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 03:28:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 03:28:20 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 03:28:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1dbbb2db815c2527e90ef5a3e4dfb957cfe7b61b6a7fc59722f1f64b1a1b611e`  
		Last Modified: Tue, 07 Apr 2026 00:10:39 GMT  
		Size: 28.1 MB (28116166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebaf10abef349ec060b1ece7fd15e26094cdfd3ee6f51c77af0c3ce86711da12`  
		Last Modified: Tue, 07 Apr 2026 03:28:41 GMT  
		Size: 91.3 MB (91288289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549e473994506979c04488d05a19a24a3a41b02ca2c4a993a0b4d8efb7a74652`  
		Last Modified: Tue, 07 Apr 2026 03:28:41 GMT  
		Size: 69.7 MB (69688954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c1fb3730f8f38530f547abd71c8663ad260c8a1b2586e2246867b0512f6854e`  
		Last Modified: Tue, 07 Apr 2026 03:28:38 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f69a27c4985fe07c4179d3c79dfbcc50f0e66ffe5143435015104a4545eec51b`  
		Last Modified: Tue, 07 Apr 2026 03:28:38 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e8a0bfd5bc88d23ffdac6e2c9538d6e9c2265600c8a3d10add11b98dde917fa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5106710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54ee7c9af683b13883cb024e19200379253cd6922a7e09392ea6bc726d734c18`

```dockerfile
```

-	Layers:
	-	`sha256:7450d467faa929eeef345cfbad25ab80cc3f1f3eff689c850a4f365a9dd57e95`  
		Last Modified: Tue, 07 Apr 2026 03:28:38 GMT  
		Size: 5.1 MB (5090043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8aa59fc9c37b2eaeba579ab7bd3e99080577567234fdfb3cb1beed9768c54e43`  
		Last Modified: Tue, 07 Apr 2026 03:28:38 GMT  
		Size: 16.7 KB (16667 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:3a4cde079bd143eca069b230330105493c3bba6e4a62f1773affbf7f697d3c9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.2 MB (199246177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c168f318a3e17800ca63024850eac17136f1edd8708d3132279ef8e4e3cb4bd5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 14:53:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 14:53:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 14:53:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 14:53:38 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 14:53:38 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 15:01:23 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 15:01:23 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 15:01:24 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 15:01:24 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 15:01:24 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b1c56220ca211bc9d02f1ed5c589465809676b6ab2cef705f1e2fb8e9726de76`  
		Last Modified: Tue, 07 Apr 2026 00:09:42 GMT  
		Size: 32.1 MB (32078464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0079b7e7e5b38775faac4e59146a115e21b13fa72289b8d54f07e7f3d4354bfb`  
		Last Modified: Tue, 07 Apr 2026 15:01:58 GMT  
		Size: 91.6 MB (91633049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c448868e422f40379ba445d994524d5f52c70d4559f190ab5c57d7b371131b03`  
		Last Modified: Tue, 07 Apr 2026 15:01:58 GMT  
		Size: 75.5 MB (75533623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a53609bf1ddda26d831c18f37e6b59b8cf5b30e18c2ee874d42f73da181ef5`  
		Last Modified: Tue, 07 Apr 2026 15:01:54 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ea195650c1a0d5444fe999edfda589fa2552737a4523a3240d06484588f4e9`  
		Last Modified: Tue, 07 Apr 2026 15:01:54 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a159232affed340d45a4e14663e24233240be9927fe1a54139a70209db4c4334
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5089328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0be36e2e9385408487c6d4d2ad64fe36e9de0b020fd15abde23c287eb7b07ad4`

```dockerfile
```

-	Layers:
	-	`sha256:31171a0f8374349ea2f376c81c6feffd301f873ef3d7bbce3151839d42b061cf`  
		Last Modified: Tue, 07 Apr 2026 15:01:55 GMT  
		Size: 5.1 MB (5072743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7843d4bb9326d703a1a8e594df13d0e8a1aeab39377648424cbb2d6a835e116`  
		Last Modified: Tue, 07 Apr 2026 15:01:54 GMT  
		Size: 16.6 KB (16585 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:73273704b9e321463f60c9e784a3381388e8e575de5e92ca181c75955ca7a338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.6 MB (183640130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb2cfbd26950e8b410a2c3196a6455ee22abb9fc85bcf020f244d0049097ace3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 05:46:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 05:46:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 05:46:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 05:46:59 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 05:46:59 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 05:48:14 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 05:48:14 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 05:48:14 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 05:48:14 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 05:48:14 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c23087fbbda0d8352ee6b2d159c503459acb89da0eba1729b411ca394e68e292`  
		Last Modified: Tue, 07 Apr 2026 00:10:59 GMT  
		Size: 26.9 MB (26891634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:895f0bd5b46fffbb9e02ff0294ffe05b5d8ea2bda03f3d8de4ef718fdba06540`  
		Last Modified: Tue, 07 Apr 2026 05:47:38 GMT  
		Size: 88.2 MB (88233804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d10a2090235b0dcd77fb83f2db91c6d065bb8f3c43d978c5ac033f8fcf0ddf02`  
		Last Modified: Tue, 07 Apr 2026 05:48:39 GMT  
		Size: 68.5 MB (68513651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f726d01d6086c9801cb9577ee8d6fab46e78f3a8490ac0a7f5e3aa5532d9d526`  
		Last Modified: Tue, 07 Apr 2026 05:48:37 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee0daa7b5d8399e5f31f6d38a4b72bb632ac86af788f2ddfd3c02311695317f5`  
		Last Modified: Tue, 07 Apr 2026 05:48:37 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:401cf76339701654520f6939296ef0a39481c2077c562785fb3b466f86d78c2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5076669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01ebe7119691c76e1142e6ecbb9c1c0fe15705f92a2166594dab3055fbab34df`

```dockerfile
```

-	Layers:
	-	`sha256:5d16ae2589d333c92b63ae0d37ee07fdb1962067984781a68f503967baaceb5f`  
		Last Modified: Tue, 07 Apr 2026 05:48:38 GMT  
		Size: 5.1 MB (5060144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4c90599c2d554abf709ea5fa8dcd1fb556604c1897d8cd83246d25e44427049`  
		Last Modified: Tue, 07 Apr 2026 05:48:37 GMT  
		Size: 16.5 KB (16525 bytes)  
		MIME: application/vnd.in-toto+json
