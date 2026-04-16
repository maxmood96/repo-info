## `clojure:tools-deps-1.12.4.1618-bookworm-slim`

```console
$ docker pull clojure@sha256:453a6accbe38a065151f66e1d60d1f7de80ac524b2d136746d0f020451e39494
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

### `clojure:tools-deps-1.12.4.1618-bookworm-slim` - linux; amd64

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

### `clojure:tools-deps-1.12.4.1618-bookworm-slim` - unknown; unknown

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

### `clojure:tools-deps-1.12.4.1618-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:924cb9539990cba155760bf9f861d85fb0f0ba264ef7d903d226ea9feb4a3994
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.1 MB (189096558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e162f11d726bf1eb14fcaea2b574ed313fdc97818a81b0f623bad0a4f6d9ed2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Wed, 15 Apr 2026 22:18:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:18:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:18:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:18:17 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:18:17 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:18:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:18:32 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:18:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:18:32 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:18:32 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1dbbb2db815c2527e90ef5a3e4dfb957cfe7b61b6a7fc59722f1f64b1a1b611e`  
		Last Modified: Tue, 07 Apr 2026 00:10:39 GMT  
		Size: 28.1 MB (28116166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f94dc77f38f4c056130c872d76c2a44360df6ee9c4f106b284a49aacd986918a`  
		Last Modified: Wed, 15 Apr 2026 22:18:53 GMT  
		Size: 91.3 MB (91288271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aba6700d4049da5089d33efa60d27ca3f3640672a75c79a6d1a5a3e722bc5bc`  
		Last Modified: Wed, 15 Apr 2026 22:18:53 GMT  
		Size: 69.7 MB (69691082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986c9d436f0af92663da4898f483785bde5f09bed6f180c211f3e11c59a7d22c`  
		Last Modified: Wed, 15 Apr 2026 22:18:49 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b59c285d038a671b991d2f24e44e0e09706eebbcfe9ec333cc9c01cd1bb5022`  
		Last Modified: Wed, 15 Apr 2026 22:18:49 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1618-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:086cff321b60186fa301ecd976a331941fea04f6554a8445e3e9debfd169790c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5106710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c32c01b63146833f109baab077222a1f6f27b6f5ad5e243ded5accf2050bb1b8`

```dockerfile
```

-	Layers:
	-	`sha256:e8322096970c2f97bb3d315b8159fdbf551df93feaef15aa0a0097ddf4c3d7df`  
		Last Modified: Wed, 15 Apr 2026 22:18:49 GMT  
		Size: 5.1 MB (5090043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fca8511a00bc92397bcdff7561dc85a84346fb89f50bc5e34c1076756b0a03ae`  
		Last Modified: Wed, 15 Apr 2026 22:18:49 GMT  
		Size: 16.7 KB (16667 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.4.1618-bookworm-slim` - linux; ppc64le

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

### `clojure:tools-deps-1.12.4.1618-bookworm-slim` - unknown; unknown

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

### `clojure:tools-deps-1.12.4.1618-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:6238e44cd4edac9cabb50d0291d84b84d726f76678bd9ceb9ca4cd3bb3b33b4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.6 MB (183639319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec9ca72211b4d9cf28bc44ecf5a4264b9c32c5ea5f4b75bd9c7aed06e79d85fb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1775433600'
# Thu, 16 Apr 2026 00:43:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 00:43:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 00:43:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 00:43:49 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 16 Apr 2026 00:43:49 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 00:45:00 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 16 Apr 2026 00:45:01 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 16 Apr 2026 00:45:01 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 16 Apr 2026 00:45:01 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 16 Apr 2026 00:45:01 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c23087fbbda0d8352ee6b2d159c503459acb89da0eba1729b411ca394e68e292`  
		Last Modified: Tue, 07 Apr 2026 00:10:59 GMT  
		Size: 26.9 MB (26891634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a78ac609f8f046c6a31d61cf5e496d160fb1bf38a5cda92b8f538e5fc85bfd`  
		Last Modified: Thu, 16 Apr 2026 00:44:26 GMT  
		Size: 88.2 MB (88233823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c0ec5c98363b0741c220393269c785f74da4bc8f4c8318d3a2879a2b0ca435b`  
		Last Modified: Thu, 16 Apr 2026 00:45:25 GMT  
		Size: 68.5 MB (68512818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:731a36ab7ac149be7871eb0b24f994b47dcc46a3e27698767808ceea9b4d9db3`  
		Last Modified: Thu, 16 Apr 2026 00:45:24 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65df5bda0c960ad8db49f2f61b65342578cf767a8142bd56c147a12b2a86a48e`  
		Last Modified: Thu, 16 Apr 2026 00:45:24 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1618-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2e2b4678e591636fafc6af5b0ca5f4cca5e2bf70925d96d65a00469a872ef924
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5076667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c5dc25b633e6ad8104000600bc73be253250d270874138b5dfad00edd315534`

```dockerfile
```

-	Layers:
	-	`sha256:22da8d77210cf1f05a06521c4cdcaa48709c0129351a1568650114f0455eef20`  
		Last Modified: Thu, 16 Apr 2026 00:45:24 GMT  
		Size: 5.1 MB (5060144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38aadbb431004a05331fd83df6919530f0cc2969f01c8d09e7680b4a76f068eb`  
		Last Modified: Thu, 16 Apr 2026 00:45:24 GMT  
		Size: 16.5 KB (16523 bytes)  
		MIME: application/vnd.in-toto+json
