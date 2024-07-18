## `amazoncorretto:17-al2-generic-jdk`

```console
$ docker pull amazoncorretto@sha256:537863940776cac25a6a39cb073a53ed7905814cca5e9c118921ce6cd5a71cf4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-generic-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:84f38679c2ec8f573254699a2c740662fe9db7c5804907849fbea8b6d1bdaaa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.9 MB (214854409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85604f05a149597e1f1b9db4b2ae128b5852ff7f64cfeef4527f9e33ff96df40`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Jun 2024 00:19:55 GMT
COPY dir:db8dc48874881c2542c8e2120173f53413158e7da7526edf07aa742f426b8c16 in / 
# Fri, 28 Jun 2024 00:19:56 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=17.0.12.7-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=17.0.12.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:2a5dc0ac7266321476902a4277a4723285b608c065fcb80cacdb3ed43a7c29fe`  
		Last Modified: Fri, 28 Jun 2024 00:20:37 GMT  
		Size: 62.6 MB (62646638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fba077306927217ceec170afa6dda754cb72b423618bc29f6fc8bfcd3ceef6b5`  
		Last Modified: Thu, 18 Jul 2024 00:56:13 GMT  
		Size: 152.2 MB (152207771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-generic-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:26b74b7616a58675e3d8a7c404c01a0abf3c87818dba959e9dce50189bfa1c59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5537954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbd75eb4020a7d8493c7128429bec1775454f0f08ddcfc6108c36f442c645d33`

```dockerfile
```

-	Layers:
	-	`sha256:4a5ae156fd98b1db667e8b0976245a39064c585e5f734a98a54b9603a256ef8c`  
		Last Modified: Thu, 18 Jul 2024 00:56:09 GMT  
		Size: 5.5 MB (5526938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9c9079572f4421dcc3e932a62d782af951437d136aa5d84641d181409f38dc0`  
		Last Modified: Thu, 18 Jul 2024 00:56:09 GMT  
		Size: 11.0 KB (11016 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-generic-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:1216b579a4bdb0b96c4c56d85f2cc5180f0a0967a7287cd749fa1acfc5cebf2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.4 MB (215433237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62d54ea8cf3a914eb2ea2131c86ba5300f1d7026360c1e699df90230900862da`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Jun 2024 00:40:02 GMT
COPY dir:36542351efcfebe46f7ccbf0def8f62c4d1fc618b41a02b6d9df97e06c5cf74a in / 
# Fri, 28 Jun 2024 00:40:03 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=17.0.12.7-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=17.0.12.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:2936210a619ec662b53521cc3dd41798a491971a48e14f14ebb594e81dc798b0`  
		Last Modified: Fri, 28 Jun 2024 00:40:34 GMT  
		Size: 64.6 MB (64568765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330afd10473cfcaf0bfbb876030ed06b9b7af4d641072846abfdd83df829a5fb`  
		Last Modified: Thu, 18 Jul 2024 01:10:17 GMT  
		Size: 150.9 MB (150864472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-generic-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:86468af032be57230299689e1641dbbc5d2b31b1ead5db8e45c943519276f5e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5536990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc2f8366fbbb309c9bd9883998150fcbd6af2a50788c2d1ff4b932007783f2ac`

```dockerfile
```

-	Layers:
	-	`sha256:6956da218adf50688bc85f05417b1679f4ff4dc58849cad3424af0f387485074`  
		Last Modified: Thu, 18 Jul 2024 01:10:13 GMT  
		Size: 5.5 MB (5525625 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ff70c5307dec94bad5e0f123073ac78337b109c07834576d8c079f0d1ca0e5b`  
		Last Modified: Thu, 18 Jul 2024 01:10:13 GMT  
		Size: 11.4 KB (11365 bytes)  
		MIME: application/vnd.in-toto+json
