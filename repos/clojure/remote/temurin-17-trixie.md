## `clojure:temurin-17-trixie`

```console
$ docker pull clojure@sha256:50c361781f83a1f57f26fa027d4b74d481550bfa5c50f8306cf81b46c425e77d
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
$ docker pull clojure@sha256:8ce6b2e20c68ea819d78954bd1dc29e8b22e1ecb2baafcde01d6f64364ee33fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.5 MB (279505332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b75dbf87cae84ad09a962c050ea656749c4e69ca5168b0a4076c6c3ba8ff710`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:80b7316254b3093eb3c7ac44bb6c34bde013f27947c1ed8d8afe456b957ebfdb`  
		Last Modified: Tue, 12 Aug 2025 20:45:14 GMT  
		Size: 49.3 MB (49278280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0c7a642b3afc77db54eb51a746581f626f572323e229ff63a2fc9bbe776bc16`  
		Last Modified: Tue, 02 Sep 2025 00:17:42 GMT  
		Size: 144.7 MB (144693268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76f79ac6eb6f4ea26dfc60aed2d70eb75287b178285565363821932fa00ed6ec`  
		Last Modified: Tue, 02 Sep 2025 00:17:41 GMT  
		Size: 85.5 MB (85532737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a6652616b46b5b969c453f50cf43705fbdf279bdd8d991f77ee56de14b916f`  
		Last Modified: Tue, 02 Sep 2025 00:17:40 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3018409d1fc3571ef78a9dde97de431436cbcf20348e5f5855f4e901d696eb30`  
		Last Modified: Tue, 02 Sep 2025 00:17:40 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:45ba410aca790222b68d96b048e1db2f9ff2bc249204bbbfdda57b25378a1e28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7478018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0c0f15cfe5224cf9bd4b15fc3bd347562f51d5707d7db7ea6cea88fed157a21`

```dockerfile
```

-	Layers:
	-	`sha256:68b64d6537a6daea405db5b3d4de35d05ac85caa7712b674e84e64d4317fbd08`  
		Last Modified: Tue, 02 Sep 2025 03:40:13 GMT  
		Size: 7.5 MB (7462221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ca7a230654baab79135d391b37376e64bb5ce39d8a57b9827eaa0f447e0e031`  
		Last Modified: Tue, 02 Sep 2025 03:40:14 GMT  
		Size: 15.8 KB (15797 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:fc262fac446336a4781f7cb2d6a3edaee6cb24759dfcdc59637ecc218db881ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.5 MB (278541184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5bdf500773e7103ca84ee77e21c3e886647cb1fa49122ca86140f6ec575c565`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d1e40442030765a3ac5d135c39154d052eba20953ea0e5d35a066f7722cdd93d`  
		Last Modified: Tue, 12 Aug 2025 22:12:36 GMT  
		Size: 49.6 MB (49641603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1b4924db0e9a6507273f53942c071f009dd0878c2430f6b5b0b67f21e1720a`  
		Last Modified: Tue, 19 Aug 2025 03:42:04 GMT  
		Size: 143.5 MB (143542131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05db609fb51f2324e9acdeab42b7b5d75aee45c26373daa1515d985d3fd907fd`  
		Last Modified: Tue, 26 Aug 2025 22:19:53 GMT  
		Size: 85.4 MB (85356406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4292a988e9c8649e6d7a10a728315f169a7b42961205082e7d9b38f3c1f99e8e`  
		Last Modified: Tue, 26 Aug 2025 18:38:09 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9226399e1ebb75e73c7dc2d3e96470d76f7a4629a3a624c1329fc6f3ae74ca03`  
		Last Modified: Tue, 26 Aug 2025 18:38:10 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:a0354c57e90e68113e698558634d11f8ea415c15e6a259f581a8a3acaa01a14f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7485166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e13e630667b60776bf1b23d5eb5744e0274147187d40c008b4107fe8ce257f22`

```dockerfile
```

-	Layers:
	-	`sha256:9cab88b4e9ed8f1957501f050811b6169b53acd278f887f54f6f27f18b4bf392`  
		Last Modified: Tue, 26 Aug 2025 18:38:57 GMT  
		Size: 7.5 MB (7469251 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b2fbdd5ab8d31f28380498e741773790a7b136a396fea1833ffccfe203e95b5`  
		Last Modified: Tue, 26 Aug 2025 18:38:58 GMT  
		Size: 15.9 KB (15915 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:9b0879540dddcd55dbbea37dc77aa4bc5f812ca093612588ed8eaa440127a21a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.4 MB (288417727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe9938387e3c53b4ff6730434127286d041a6d09ebfd6b1f90fea8983488b1b4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:befe77620590f63939f5bcadadc9f45832981822c9c901f057eb4e86f733c29a`  
		Last Modified: Wed, 13 Aug 2025 00:32:04 GMT  
		Size: 53.1 MB (53103384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5096f4531428918861fb2e9c0966a5ff7b6e852e32764913f3a77fdb5d16a0d6`  
		Last Modified: Sun, 24 Aug 2025 02:07:43 GMT  
		Size: 144.4 MB (144372854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ea8a03eb35599ce7b7a3e8915476b84cde92615e3921a0f772632b4e9bd6e81`  
		Last Modified: Tue, 26 Aug 2025 18:01:04 GMT  
		Size: 90.9 MB (90940443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfab0c62332a53bce027b48e762792876212411be87c1c277d1fdd0695bc6391`  
		Last Modified: Tue, 26 Aug 2025 18:00:51 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbca8021777bf4e0d0f27fd4005137b247fe2a261e8613aebbd4e497fcb9d54d`  
		Last Modified: Tue, 26 Aug 2025 18:00:51 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:12a5080ee4f4d1cd5600888351bc5cd557e099faa464c76a452e44d61e1caed6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7482485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7ce30b972a1ee6050d4da1de8c0581f7a229ef72468e5c2350aec960bc5edf2`

```dockerfile
```

-	Layers:
	-	`sha256:74d5e6d15cca13051f90fbad7c972056a5b43fb0c30cc2733eac6c48ec76473a`  
		Last Modified: Tue, 26 Aug 2025 18:39:04 GMT  
		Size: 7.5 MB (7466640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7d483c83d30ac5cf79ed8e07c2fc42edf14b8b22d0371fed46c4e988d18c30d`  
		Last Modified: Tue, 26 Aug 2025 18:39:05 GMT  
		Size: 15.8 KB (15845 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:15dcf974f510d4cd4bb2270f9f0164e61ff8a566733acfe20e8b97c776b805a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.8 MB (270766201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e95a0e35e9ab976b993d7fc753ecedebaff88ff8a541118c26885af11419ab3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:59f3e0adb655cb03f7d489f3cc57e302e249916bbb076c78008f9329238bfb20`  
		Last Modified: Wed, 13 Aug 2025 01:13:55 GMT  
		Size: 47.8 MB (47764303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d0498801f7d069ee03e6b4b2295a44eca76d9f1c80a0378ec99d41a263986c4`  
		Last Modified: Sun, 24 Aug 2025 02:08:04 GMT  
		Size: 138.6 MB (138575686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a2eeee7d2142d2db5be4153d0b018726d7ea1d5e940740027fa39195e02daad`  
		Last Modified: Wed, 27 Aug 2025 09:06:24 GMT  
		Size: 84.4 MB (84425167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:255778b16ddb5c18150e78da3c0824807d1095bf3ca1ebd8d5b9f7c90f4485cf`  
		Last Modified: Wed, 27 Aug 2025 09:06:20 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1573b3b133c7e5cffd3cde541bd825f5c6c62752833d828121f90bc8ecd0f530`  
		Last Modified: Wed, 27 Aug 2025 09:06:20 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:377e5fee5c25f86d8857e0c6c147120be68b066e101e7738072c4cd38a36b411
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7464060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61399ea534a3e015b729da7fa22267f38ef580c64a56e3c74609f6effb09ab48`

```dockerfile
```

-	Layers:
	-	`sha256:85ce3d60bc0a8e94580dc257de88dfaeece7c8ce722771cd053049e4088a6897`  
		Last Modified: Wed, 27 Aug 2025 12:35:44 GMT  
		Size: 7.4 MB (7448215 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c67f85370224c85d063a13bb6deab2fcda8fea33a9c1563cef297897efce11fc`  
		Last Modified: Wed, 27 Aug 2025 12:35:44 GMT  
		Size: 15.8 KB (15845 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:edfc6a1f3c76a1e19a641dcda86e2d1f9502349c673ce85d5f41d3740f238998
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.6 MB (270568919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d009ae41a224cdc4661b295a05131399231a2d15ad08de9669c11579bcdd32f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c3b791adea90b39bc59919a9959b7f44f65aa3364a03dd0271a5ff658488877f`  
		Last Modified: Tue, 12 Aug 2025 20:59:03 GMT  
		Size: 49.3 MB (49345161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ad91519ab3afcb86eb1e7437e5a1429cf6a5c21c2087fabcb2a282473cb2bb`  
		Last Modified: Tue, 02 Sep 2025 02:00:44 GMT  
		Size: 134.7 MB (134724230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a50a94b3529eed0f0d1bb0d95341ab15278de3ba16c625aa9fa5f14ff8afeac`  
		Last Modified: Tue, 02 Sep 2025 02:07:03 GMT  
		Size: 86.5 MB (86498487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1bb02e452edd1a0cf7ebcee35daa1d4e2328d3e04522bd49021ad30bf3c65e`  
		Last Modified: Tue, 02 Sep 2025 02:06:53 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a15ef4d8f091bc6400ea52459d5a0ffc0d20fdb8e8a3aa4ef249862d512f150f`  
		Last Modified: Tue, 02 Sep 2025 02:06:53 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:812136c17b083d67603110a43e95c2a84743b554f5a1b3222c4ae48f713e1f6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7473940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6f31ac29a399b9d64f5764f9cd6e7c50ef4cdd79bbb25cbad7f45540f67eedb`

```dockerfile
```

-	Layers:
	-	`sha256:d1d976376a55dc2494ece5175d3de6fdaa64a2390c3df1d99f9578061d5f37de`  
		Last Modified: Tue, 02 Sep 2025 03:40:38 GMT  
		Size: 7.5 MB (7458143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d674c518e42b3e10efedb29e012f038f90fb354faae2104357a284662ff94d2`  
		Last Modified: Tue, 02 Sep 2025 03:40:40 GMT  
		Size: 15.8 KB (15797 bytes)  
		MIME: application/vnd.in-toto+json
