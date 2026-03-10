## `clojure:temurin-17-tools-deps-1.12.4.1618-trixie`

```console
$ docker pull clojure@sha256:b19ed500dbd7345fdf48d04259b6dfb6120b02bb4652ec3a411f010b7d5fddf9
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

### `clojure:temurin-17-tools-deps-1.12.4.1618-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:ec0888798a9ae8eef1e6e8b776ed0359d683a8c8d06be37bdc7f35976f777098
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.5 MB (280490250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:364c001d55fa8500273dff9d7812181e6b62c5b181540657cba98bf1aab03139`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Mon, 09 Mar 2026 20:35:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:35:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:35:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:35:24 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:35:24 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:35:42 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:35:42 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:35:43 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 09 Mar 2026 20:35:43 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 09 Mar 2026 20:35:43 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:866771c43bf5eb77362eeeb163c0c825e194c2806d0b697028434e3b9c02f59d`  
		Last Modified: Tue, 24 Feb 2026 18:43:22 GMT  
		Size: 49.3 MB (49293124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6175f29ccc7125b0de9390ab22d534dfb7361f1497b4635184c790c94c6aa6da`  
		Last Modified: Mon, 09 Mar 2026 20:36:06 GMT  
		Size: 145.6 MB (145628703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab9e2961f2a000a10207df2be5a7b920212386be20f9716d79bfbbcb73dc9465`  
		Last Modified: Mon, 09 Mar 2026 20:36:05 GMT  
		Size: 85.6 MB (85567380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee9da42abd24fa28046053e81a17c7a516c66c68f83b379708f6abe5318da3c0`  
		Last Modified: Mon, 09 Mar 2026 20:36:02 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85bc38f32a95afe79ba4b78afa29e28277fcf8e1e2d7954c009d03cd3c674631`  
		Last Modified: Mon, 09 Mar 2026 20:36:01 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:1d0075d0465a5fbd4a180db9271a24d4cc0814ac8e1db83a346c3de4968cbf61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7486347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52bb56e5bb97750c8434342ed49bdac162a32577ef72d2f4e753f3b0dece87ba`

```dockerfile
```

-	Layers:
	-	`sha256:b47ee6bc6d8d521cadaa99f68d3f68112e851b2756dd684f89558abbff0ddf85`  
		Last Modified: Mon, 09 Mar 2026 20:36:02 GMT  
		Size: 7.5 MB (7470593 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:072271e3eafaa3a4975be817ceea22de7fd9ef59cd6b61b3f200d718b81d6a00`  
		Last Modified: Mon, 09 Mar 2026 20:36:01 GMT  
		Size: 15.8 KB (15754 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1618-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0d8f91e070cff3cdaa5fe5f99fce429ddfe255aa4396de6af0e1446ce5039610
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.5 MB (279472208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ad2a457ffb54982ae994f486b145f84ab27d8b81b072719d036efe399b0405f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Mon, 09 Mar 2026 20:35:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:35:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:35:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:35:12 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:35:12 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:35:31 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:35:31 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:35:31 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 09 Mar 2026 20:35:31 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 09 Mar 2026 20:35:31 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ac9148dc57ca750b09f3f3da6f16324e1a3b62432b2726734535ec610e1a9232`  
		Last Modified: Tue, 24 Feb 2026 18:42:56 GMT  
		Size: 49.7 MB (49652168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e599f818486500570d94d35208982042e971b3946fce520547f21a2d1af07a`  
		Last Modified: Mon, 09 Mar 2026 20:35:55 GMT  
		Size: 144.4 MB (144436184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3de387f55dd819409664cfba32883b4d164f4a767dba6156c8cb8536abb8ad42`  
		Last Modified: Mon, 09 Mar 2026 20:35:54 GMT  
		Size: 85.4 MB (85382811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37cc9317dec9a7fb8f87d40d793845afef24ac2ea9150ef5e4ee85cf458940e4`  
		Last Modified: Mon, 09 Mar 2026 20:35:51 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce721f5e35517a73b0cb6a44d03fe9c5b5a6cbd70b0b6a356e4d028273aa94f`  
		Last Modified: Mon, 09 Mar 2026 20:35:51 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:f5d790fdc4d8f38e0f3ab7752f766ca0340d7708dd97c763c90ebb364426af99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7493495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13a0c75965055a7d73a432e73899dc3236982225fbe7c9f01574124f97d17a01`

```dockerfile
```

-	Layers:
	-	`sha256:ee0ae5b2a37a7de63473989925e65ae8cf02b376caa182a8d67cf70db80028ed`  
		Last Modified: Mon, 09 Mar 2026 20:35:51 GMT  
		Size: 7.5 MB (7477623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8230552f6e9402f2683c83b10efd4e62e858a7062bf1511c0c1767e785e864e4`  
		Last Modified: Mon, 09 Mar 2026 20:35:51 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1618-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:bddb9df7df87ef95ac3459235d08ae129926b3c5cc3ccc48b7cdadee1276358c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.5 MB (289528095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:528d55849a428d77a6f0c6cd80a2fffd5ffb7d2b8dcf32e24300f338b5d1383c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Mon, 09 Mar 2026 20:54:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:54:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:54:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:54:24 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:54:26 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:55:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:55:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:55:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 09 Mar 2026 20:55:33 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 09 Mar 2026 20:55:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:468eb7cd0e9ceb9e5b1c4c9daadd36c2fd1f1ee82c667dc1a7d70fa95600a20f`  
		Last Modified: Tue, 24 Feb 2026 18:45:11 GMT  
		Size: 53.1 MB (53112261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa68eefccf52feae213c365bd35426d2716c52016a1ead8472aed0ffcacc64c0`  
		Last Modified: Mon, 09 Mar 2026 20:56:25 GMT  
		Size: 145.4 MB (145438177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fd88027fdb0a73e7821484ecb535361a5f5a05f0f77ab8f269390b8349b7024`  
		Last Modified: Mon, 09 Mar 2026 20:56:25 GMT  
		Size: 91.0 MB (90976614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a2f0af1a45089a1861b447771d51340708e3fb00682d26d1679459aad59944e`  
		Last Modified: Mon, 09 Mar 2026 20:56:21 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ea1779e7a8784a0b84029276a56471700b7e9d7250bc5a946cbe09d448e412`  
		Last Modified: Mon, 09 Mar 2026 20:56:21 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:089a6806c7dd4b1a94e1544b527ba134624b04fb5e6c8128ad0da744143897cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7490816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2776756d3c79627afe612b34d6bd69606ec9d77e37fb21e2ad75eab888037ec`

```dockerfile
```

-	Layers:
	-	`sha256:be74f7e5ab538f7814c096a584e9e1ecdcffd9d79402faf51c579d71829b4c15`  
		Last Modified: Mon, 09 Mar 2026 20:56:21 GMT  
		Size: 7.5 MB (7475014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d7d3f0f4a7b6327f92112d5b7f0369643998bab5395078edf1fa762f4424b00`  
		Last Modified: Mon, 09 Mar 2026 20:56:21 GMT  
		Size: 15.8 KB (15802 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1618-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:3c41d4f3ca65ef7273b1dacb0af0f7202d77fbddd9b1e70f199868f285ae87cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.5 MB (271512229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f95d22b086a6b1b2403f0ab0696ace901c55dc7fd630899497242d2f235a6f06`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Mon, 09 Mar 2026 20:34:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:34:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:34:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:34:35 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:34:35 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:34:50 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:34:50 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:34:50 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 09 Mar 2026 20:34:50 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 09 Mar 2026 20:34:50 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:aba9aa950add2749194487d5c63a3069af6daf9dfe54d80cfbe32bfa7a5faa07`  
		Last Modified: Tue, 24 Feb 2026 18:43:53 GMT  
		Size: 49.4 MB (49354534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1cbcb5248fc503b481bbe2b07eb7cd2334c8d5ac0ebd99cd90c571d63224ae6`  
		Last Modified: Mon, 09 Mar 2026 20:35:21 GMT  
		Size: 135.6 MB (135627117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0390e971b5192ef338a1ff5971e2331432a502855c66612de614355efc34e2c`  
		Last Modified: Mon, 09 Mar 2026 20:35:20 GMT  
		Size: 86.5 MB (86529536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bffdb90a87991374b3269050c89544c0e5d14fb8331b1108d0141c8e84f1a449`  
		Last Modified: Mon, 09 Mar 2026 20:35:18 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5a78a6295474b2f6f0a873135519e982120a15cf7d6f01d0d0595528ec0daf`  
		Last Modified: Mon, 09 Mar 2026 20:35:18 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:e85bb88d65c7bb3dd7a92c075df327c136472f77ce099ee661f2f96f41da6e78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7482269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff50865e20ae029bb021cbea06a4a112a4b2e392a4f5f1c0b9666b20433cf4ec`

```dockerfile
```

-	Layers:
	-	`sha256:c35740b394e84cc0780df2c241502fefb547c6f4a10186ada25ca235aa3b5b86`  
		Last Modified: Mon, 09 Mar 2026 20:35:18 GMT  
		Size: 7.5 MB (7466515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce966776320fbf4f44edbee44a79695f75ce3f740231cb3c621f7462a8707b55`  
		Last Modified: Mon, 09 Mar 2026 20:35:18 GMT  
		Size: 15.8 KB (15754 bytes)  
		MIME: application/vnd.in-toto+json
