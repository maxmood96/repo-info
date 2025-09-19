<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:8.17.10`](#elasticsearch81710)
-	[`elasticsearch:8.18.7`](#elasticsearch8187)
-	[`elasticsearch:8.19.4`](#elasticsearch8194)
-	[`elasticsearch:9.0.7`](#elasticsearch907)
-	[`elasticsearch:9.1.4`](#elasticsearch914)

## `elasticsearch:8.17.10`

```console
$ docker pull elasticsearch@sha256:13fdd468ca81f79617206311390d1e4a3fc152622532104c8aaae188ea22fab6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.17.10` - linux; amd64

```console
$ docker pull elasticsearch@sha256:0a07d580f8cd0c59ba5aae4150a1ae8a961ea1bb0f4df8875d527f33ee30f6e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **677.0 MB (676958603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25770b96ec32fa1b2b96dda9a04fe8ef8dee4200255df6b56bfe8b0cd9b75eba`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 12 Aug 2025 08:18:47 GMT
ARG RELEASE
# Tue, 12 Aug 2025 08:18:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Aug 2025 08:18:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Aug 2025 08:18:47 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 12 Aug 2025 08:18:47 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Tue, 12 Aug 2025 08:18:47 GMT
CMD ["/bin/bash"]
# Tue, 12 Aug 2025 08:18:47 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Aug 2025 08:18:47 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 12 Aug 2025 08:18:47 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 08:18:47 GMT
ENV SHELL=/bin/bash
# Tue, 12 Aug 2025 08:18:47 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 12 Aug 2025 08:18:47 GMT
LABEL org.label-schema.build-date=2025-08-08T08:36:52.872377389Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=e5c4b2af120c131ea2885730f6693cb7d40a0a63 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.17.10 org.opencontainers.image.created=2025-08-08T08:36:52.872377389Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=e5c4b2af120c131ea2885730f6693cb7d40a0a63 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.17.10
# Tue, 12 Aug 2025 08:18:47 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 12 Aug 2025 08:18:47 GMT
CMD ["eswrapper"]
# Tue, 12 Aug 2025 08:18:47 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:640ff32a54f918f74cc020f75f317b622a794ae769178b9bf55bf3250bda8e62`  
		Last Modified: Tue, 16 Sep 2025 00:56:26 GMT  
		Size: 4.5 MB (4493772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26028e086680c014f5824215ec92e59ee544f545ac62fec3d9e354704dbef508`  
		Last Modified: Mon, 15 Sep 2025 22:54:43 GMT  
		Size: 3.5 KB (3523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4902e8916b5631c52be14f509b3d5e1dc9f4389683a9fb4dc8f6d1094ac1198e`  
		Last Modified: Tue, 16 Sep 2025 00:57:02 GMT  
		Size: 642.4 MB (642446694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97cad21a7b9fa8a6cb667eece750784d61bd1b96548cac9f9b8e80157b15c5af`  
		Last Modified: Mon, 15 Sep 2025 22:54:42 GMT  
		Size: 9.5 KB (9532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c46cf9f99528689ca96a295ddb7807def9e4f2b65fd1bae43790e50c2950a71`  
		Last Modified: Mon, 15 Sep 2025 22:54:43 GMT  
		Size: 1.7 KB (1715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b09c2bd59b36911d13bfabf6944a6323eeaee622fb9a0e03d920a0046ccde7d`  
		Last Modified: Mon, 15 Sep 2025 22:54:43 GMT  
		Size: 163.9 KB (163939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70508771870a2a76f79778bc8c276b2a8d24714486412b9b6e7c1d0270c6120`  
		Last Modified: Mon, 15 Sep 2025 22:54:43 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:372b5524dcd9dfd49129df1249a0cff1da90f07055282b5073ecae2ab5de3c04`  
		Last Modified: Mon, 15 Sep 2025 22:54:43 GMT  
		Size: 115.5 KB (115541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.17.10` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:99bfc06aba908a120bbb63f41c9de27b90637c5948d10b3456f32c4107af7b07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3203181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c507ddd11348d47d2ad5ff7346464031c7e9dd666d76fa948d52dba91942fbc8`

```dockerfile
```

-	Layers:
	-	`sha256:c883b0d7e3b167b8223e0f3aa4ae035dd9a96fd969895d48c36636c645ba4043`  
		Last Modified: Tue, 16 Sep 2025 00:25:21 GMT  
		Size: 3.2 MB (3164785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80ac70da27c7d59eb3fb5e2d328c085a3e77839d20fafc2b06351d3ec1826c2e`  
		Last Modified: Tue, 16 Sep 2025 00:25:21 GMT  
		Size: 38.4 KB (38396 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.17.10` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:d0cef9a4db6b00df5bab650ad8e2eaf10a7f3cde4ab9bfc37ef5a83daeb0a25a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **521.2 MB (521164753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad62af1907e1cc63f86d7b86629660f0c3a54e8d020c2ad921ea10e8ea87191c`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 12 Aug 2025 08:18:47 GMT
ARG RELEASE
# Tue, 12 Aug 2025 08:18:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Aug 2025 08:18:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Aug 2025 08:18:47 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 12 Aug 2025 08:18:47 GMT
ADD file:4e55519deacaaab35bcc389ec63f319a61c50e3f8f7d19a0df61fa1571c86c6a in / 
# Tue, 12 Aug 2025 08:18:47 GMT
CMD ["/bin/bash"]
# Tue, 12 Aug 2025 08:18:47 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Aug 2025 08:18:47 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 12 Aug 2025 08:18:47 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 08:18:47 GMT
ENV SHELL=/bin/bash
# Tue, 12 Aug 2025 08:18:47 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 12 Aug 2025 08:18:47 GMT
LABEL org.label-schema.build-date=2025-08-08T08:36:52.872377389Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=e5c4b2af120c131ea2885730f6693cb7d40a0a63 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.17.10 org.opencontainers.image.created=2025-08-08T08:36:52.872377389Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=e5c4b2af120c131ea2885730f6693cb7d40a0a63 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.17.10
# Tue, 12 Aug 2025 08:18:47 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 12 Aug 2025 08:18:47 GMT
CMD ["eswrapper"]
# Tue, 12 Aug 2025 08:18:47 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:59a5d47f84c39a2d62d1b5089e60ab67303111f17e1df01dbbcc598246282797`  
		Last Modified: Wed, 10 Sep 2025 09:09:46 GMT  
		Size: 28.9 MB (28861317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abe38c1caf84efcb49d1c8f35c73f6664b25b6d1bbaa1a6bf1e2d94d7c5d6e2e`  
		Last Modified: Mon, 15 Sep 2025 22:15:35 GMT  
		Size: 4.5 MB (4498611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d13132e82d6196648e653017276aec78bc86b058006fe9047c0d6791ed5fa350`  
		Last Modified: Mon, 15 Sep 2025 22:15:35 GMT  
		Size: 3.5 KB (3522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08dd8de22458d573705b59cd4490eaa280bd06a3f6e7cb2ee5ba279a36044e75`  
		Last Modified: Tue, 16 Sep 2025 00:26:40 GMT  
		Size: 487.5 MB (487514138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c17edb78f45ff64dd9b41bc3154f7ae543b72c56608dc03d76241869f72283c`  
		Last Modified: Mon, 15 Sep 2025 22:15:35 GMT  
		Size: 9.1 KB (9105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c2e43ecdebface168a55f3529b8a2060cc621a031dbb34affd8664fe9a0117`  
		Last Modified: Mon, 15 Sep 2025 22:15:35 GMT  
		Size: 1.7 KB (1716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2a89e9a520fab115f7c8cf1fa847764c22f66046848fa81902207462cc13e13`  
		Last Modified: Mon, 15 Sep 2025 22:15:35 GMT  
		Size: 160.4 KB (160367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ea6d323aa852f81b18d82ce3b1bbebf23d889caa0767d72caec234c8c198ea0`  
		Last Modified: Mon, 15 Sep 2025 22:15:35 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab0965346596322643c2d9f39b01c3d5123ffc28518c3ae45aca51dd9649d148`  
		Last Modified: Mon, 15 Sep 2025 22:15:36 GMT  
		Size: 115.5 KB (115541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.17.10` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:0fdb9e199b8ad95148110e53c567ccb85cefad59bfcf747107ec1d2bff280fbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3203168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:933509e76845102273e0469cced77e929e90bfea794615ea2e59c28fbe9afa7e`

```dockerfile
```

-	Layers:
	-	`sha256:bf247467f5390f0b2bc3924d9efbd8a6ec6f46419806614132ad2de1c4b3131c`  
		Last Modified: Tue, 16 Sep 2025 00:25:26 GMT  
		Size: 3.2 MB (3164569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3687854c5edf99dc87d24212be108eb0f68c2a1e0b21271e4f48cfeca830d1ab`  
		Last Modified: Tue, 16 Sep 2025 00:25:26 GMT  
		Size: 38.6 KB (38599 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:8.18.7`

```console
$ docker pull elasticsearch@sha256:37e851eb4e9b5961334b101e4d9321b56b660d40265c1540a08ea6ccc7481701
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.18.7` - linux; amd64

```console
$ docker pull elasticsearch@sha256:f77f89113321818ff8edc5976687205c8fa99744a8021370f3de6528b4179dbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **688.6 MB (688578281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1218f1732259a9a79f0bb232898f13d0003ab6491ab743f59a808c1b3426e60b`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Wed, 10 Sep 2025 05:42:32 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:42:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:42:34 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Wed, 10 Sep 2025 05:42:34 GMT
CMD ["/bin/bash"]
# Tue, 16 Sep 2025 08:32:12 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 16 Sep 2025 08:32:12 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 16 Sep 2025 08:32:12 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Sep 2025 08:32:12 GMT
ENV SHELL=/bin/bash
# Tue, 16 Sep 2025 08:32:12 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL org.label-schema.build-date=2025-09-10T22:04:56.853519418Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=4ee681e2f5c63d2cd0aea062bb3a4c247ec2ffe0 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.18.7 org.opencontainers.image.created=2025-09-10T22:04:56.853519418Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=4ee681e2f5c63d2cd0aea062bb3a4c247ec2ffe0 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.18.7
# Tue, 16 Sep 2025 08:32:12 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 16 Sep 2025 08:32:12 GMT
CMD ["eswrapper"]
# Tue, 16 Sep 2025 08:32:12 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20491585e2733c0a4f8f10343a305940643aa1e3523bfae1d0527d4eb5b0222`  
		Last Modified: Tue, 16 Sep 2025 17:57:40 GMT  
		Size: 4.5 MB (4493710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98d00ad3e5afc4a303539c67337e65127b7ccee698dd4e0c58cab46cc14e2f0b`  
		Last Modified: Tue, 16 Sep 2025 17:57:39 GMT  
		Size: 3.5 KB (3523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5708b95ffce11f852f52583ff82769ca243573934704f55fa89f5a34652c825`  
		Last Modified: Tue, 16 Sep 2025 19:01:07 GMT  
		Size: 654.1 MB (654066462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c512ca72426db19b6b9aa188c89f314cb320b1ecb78638afceec9660dafe402e`  
		Last Modified: Tue, 16 Sep 2025 17:57:39 GMT  
		Size: 9.5 KB (9530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ee0bb7f223f9ea17c3328dc55b4a3ca6393da44f8af06e47bca0642ae90013`  
		Last Modified: Tue, 16 Sep 2025 17:57:40 GMT  
		Size: 1.7 KB (1714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27d8f1566a0e3d2797163b520e1b1ff160f9f037700530804a03c7c2ef07f4d9`  
		Last Modified: Tue, 16 Sep 2025 17:57:40 GMT  
		Size: 163.9 KB (163930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f58a79d1efa9b8ff4245effd675cdf4bbc4d79a45aa0877875ad04fb177caf04`  
		Last Modified: Tue, 16 Sep 2025 17:57:40 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7ba0949e8bd299c377459477e33a74c9983c24b9ee43958caeac7873cf9413`  
		Last Modified: Tue, 16 Sep 2025 17:57:41 GMT  
		Size: 115.5 KB (115527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.18.7` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:3c576e0650f4b2b9743a557daf69f720b816f384f1b0f220a5e773acb48ecd67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3231131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eface70680383ef503cec98394941bd55ef07c34d0b0a20a89ea06421cb683dc`

```dockerfile
```

-	Layers:
	-	`sha256:e7fc19d56baa052f26dcd79a6ecb90932f2660f7ff9cbf2d3319568f58288316`  
		Last Modified: Tue, 16 Sep 2025 18:25:24 GMT  
		Size: 3.2 MB (3192742 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5410712ce12f2071e430376d6316cfc800ca04d2578249c89b0f0774366e7252`  
		Last Modified: Tue, 16 Sep 2025 18:25:25 GMT  
		Size: 38.4 KB (38389 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.18.7` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:7473b4a37e6a80e2d66e017e208b5911e035980ec6ade735d232e20922708977
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **531.0 MB (530992020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93f71ad9ae95811fcfe50e66267a7684e7ac085b9af4c49aac50801795f7479f`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Wed, 10 Sep 2025 05:45:34 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:45:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:45:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:45:34 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:45:38 GMT
ADD file:4e55519deacaaab35bcc389ec63f319a61c50e3f8f7d19a0df61fa1571c86c6a in / 
# Wed, 10 Sep 2025 05:45:39 GMT
CMD ["/bin/bash"]
# Tue, 16 Sep 2025 08:32:12 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 16 Sep 2025 08:32:12 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 16 Sep 2025 08:32:12 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Sep 2025 08:32:12 GMT
ENV SHELL=/bin/bash
# Tue, 16 Sep 2025 08:32:12 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL org.label-schema.build-date=2025-09-10T22:04:56.853519418Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=4ee681e2f5c63d2cd0aea062bb3a4c247ec2ffe0 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.18.7 org.opencontainers.image.created=2025-09-10T22:04:56.853519418Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=4ee681e2f5c63d2cd0aea062bb3a4c247ec2ffe0 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.18.7
# Tue, 16 Sep 2025 08:32:12 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 16 Sep 2025 08:32:12 GMT
CMD ["eswrapper"]
# Tue, 16 Sep 2025 08:32:12 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:59a5d47f84c39a2d62d1b5089e60ab67303111f17e1df01dbbcc598246282797`  
		Last Modified: Wed, 10 Sep 2025 09:09:46 GMT  
		Size: 28.9 MB (28861317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebc0d3dab7863e8e1fa1f077fa529092b7d1874b39dc44bf65e4574a87d0d592`  
		Last Modified: Tue, 16 Sep 2025 17:55:42 GMT  
		Size: 4.5 MB (4498711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e64eb3d21b8c3eed87d0bb92152dab86fb88f910c1439798c28617ee3e85b694`  
		Last Modified: Tue, 16 Sep 2025 17:55:41 GMT  
		Size: 3.5 KB (3521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b341334c0dbe9c358fcfb12e7ece9c04042f6279c846f23a05420134456c684`  
		Last Modified: Tue, 16 Sep 2025 18:11:03 GMT  
		Size: 497.3 MB (497341325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c392b95d82d24be2be8f33ab6b9fcf42ac135d89adb86a71e5dda04d7bc88ee`  
		Last Modified: Tue, 16 Sep 2025 17:55:41 GMT  
		Size: 9.1 KB (9105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de732e2a50b036036f6841e71f6f9084d61553c573e002467e2a13605b56666a`  
		Last Modified: Tue, 16 Sep 2025 17:55:41 GMT  
		Size: 1.7 KB (1716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56449a39509be15034022fc72d405af01f8f566c81e6e206d25ebfb810b3a4b3`  
		Last Modified: Tue, 16 Sep 2025 17:55:41 GMT  
		Size: 160.4 KB (160360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3385e868aaa166a6d97d3ba8eabb8694c45a9cc7c716271f842f540f7b4d6cb9`  
		Last Modified: Tue, 16 Sep 2025 17:55:41 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:313d1791aff9dc13b30be5424b5fc53ae99dfb0614fc66075b014d61e0b523e3`  
		Last Modified: Tue, 16 Sep 2025 17:55:42 GMT  
		Size: 115.5 KB (115529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.18.7` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:ab2600eb16e4913f050479c9c34f70461a47aa8318748869e629284f03157c19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3231747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1d03a8e1a0846e3275051d16ebafdce71c26209091354e18f0e2bf53a4224ee`

```dockerfile
```

-	Layers:
	-	`sha256:761ec85f7645ef167e08ee7f378db7fbf316e0c0219676c25fe7a4994da4ac5f`  
		Last Modified: Tue, 16 Sep 2025 18:25:31 GMT  
		Size: 3.2 MB (3193155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3bc4467033212c404752d8b830f8f486f933466c9a49144805dcc30f21aec9a`  
		Last Modified: Tue, 16 Sep 2025 18:25:31 GMT  
		Size: 38.6 KB (38592 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:8.19.4`

```console
$ docker pull elasticsearch@sha256:fc8a4ee4241b43cd52148817339aa1c8d133cd8339dae39361b7ddd2edc59548
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.19.4` - linux; amd64

```console
$ docker pull elasticsearch@sha256:3c4c1b63b7deadaaae1f4e49514ac4ecb7a4a5db3e7585b52951b1819df21726
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **695.9 MB (695883990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:871d88eb73ce6b3e45ee71fe161f99de700821e7b9d425f8d026cb0c88092804`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Wed, 10 Sep 2025 05:42:32 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:42:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:42:34 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Wed, 10 Sep 2025 05:42:34 GMT
CMD ["/bin/bash"]
# Thu, 18 Sep 2025 08:07:26 GMT
RUN yes no | dpkg-reconfigure dash && for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 18 Sep 2025 08:07:26 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 18 Sep 2025 08:07:26 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Sep 2025 08:07:26 GMT
ENV SHELL=/bin/bash
# Thu, 18 Sep 2025 08:07:26 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 18 Sep 2025 08:07:26 GMT
LABEL org.label-schema.build-date=2025-09-16T22:06:03.940754111Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=aa0a7826e719b392e7782716b323c4fb8fa3b392 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.19.4 org.opencontainers.image.created=2025-09-16T22:06:03.940754111Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=aa0a7826e719b392e7782716b323c4fb8fa3b392 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.4
# Thu, 18 Sep 2025 08:07:26 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 18 Sep 2025 08:07:26 GMT
CMD ["eswrapper"]
# Thu, 18 Sep 2025 08:07:26 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d76ba0f156b5c8a5a8780cff62628b319904b4a59745424f2c244c9a80f7cc4`  
		Last Modified: Thu, 18 Sep 2025 18:51:12 GMT  
		Size: 5.0 MB (4962732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ef5141611c306470e8605b94e5cc8b1cca5bcfa9ae8246384e790e76188ccd`  
		Last Modified: Thu, 18 Sep 2025 18:51:12 GMT  
		Size: 3.5 KB (3525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2734b339d45096a3ca3892df9556616dc7e5ecf7c0ca39d2c3606cd74938f865`  
		Last Modified: Thu, 18 Sep 2025 18:51:54 GMT  
		Size: 660.9 MB (660903143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7639518e102858853f811a93ca93be8fdf953ceb9bde947e792e8f002340d16f`  
		Last Modified: Thu, 18 Sep 2025 18:51:10 GMT  
		Size: 9.5 KB (9530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75c409e70d9358a125e945e6d9f874b98cb9488166c225f8ea67a72691d4bdfd`  
		Last Modified: Thu, 18 Sep 2025 18:51:10 GMT  
		Size: 1.7 KB (1715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a711a3e94cb76028fb216825215eec16d18bf422e43a1911218777a3ccf3c4`  
		Last Modified: Thu, 18 Sep 2025 18:51:10 GMT  
		Size: 163.9 KB (163931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a863425b29fdbe96947223227771ee63663a00a4e964399f38534808779144b`  
		Last Modified: Thu, 18 Sep 2025 18:51:12 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce92c7bdc6fc7104b2090b92413798230af10be7b12318ffdc849eb28f3d6191`  
		Last Modified: Thu, 18 Sep 2025 18:51:12 GMT  
		Size: 115.5 KB (115526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.19.4` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:805c963b13cc5b91ff7f84092a6468a59a48a067ffaa1290ab9b57b876956a04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3251086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e266cf98561c622bb37737510c4d1395df6196f50e7fd7a87452b080df99531`

```dockerfile
```

-	Layers:
	-	`sha256:2fc8599eff1472966ed4680d97a5419ab0cbcd11dc8821cf4c04244457a61935`  
		Last Modified: Thu, 18 Sep 2025 19:00:43 GMT  
		Size: 3.2 MB (3214203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3af4c7fa5be51d842a13b8f04c650484262b700529bf41ce7a0ab6493bc97b22`  
		Last Modified: Thu, 18 Sep 2025 19:00:45 GMT  
		Size: 36.9 KB (36883 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.19.4` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:624c089909d130f1c88b1b08b0a6c1903027a60e5744dab5cfe4175612948694
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **538.3 MB (538278894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8c74ef144f193b8291d9ee97a3c1f14896d26421add15f7174d0fb4a8a81beb`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Wed, 10 Sep 2025 05:45:34 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:45:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:45:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:45:34 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:45:38 GMT
ADD file:4e55519deacaaab35bcc389ec63f319a61c50e3f8f7d19a0df61fa1571c86c6a in / 
# Wed, 10 Sep 2025 05:45:39 GMT
CMD ["/bin/bash"]
# Thu, 18 Sep 2025 08:07:26 GMT
RUN yes no | dpkg-reconfigure dash && for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 18 Sep 2025 08:07:26 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 18 Sep 2025 08:07:26 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Sep 2025 08:07:26 GMT
ENV SHELL=/bin/bash
# Thu, 18 Sep 2025 08:07:26 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 18 Sep 2025 08:07:26 GMT
LABEL org.label-schema.build-date=2025-09-16T22:06:03.940754111Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=aa0a7826e719b392e7782716b323c4fb8fa3b392 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.19.4 org.opencontainers.image.created=2025-09-16T22:06:03.940754111Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=aa0a7826e719b392e7782716b323c4fb8fa3b392 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.4
# Thu, 18 Sep 2025 08:07:26 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 18 Sep 2025 08:07:26 GMT
CMD ["eswrapper"]
# Thu, 18 Sep 2025 08:07:26 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:59a5d47f84c39a2d62d1b5089e60ab67303111f17e1df01dbbcc598246282797`  
		Last Modified: Wed, 10 Sep 2025 09:09:46 GMT  
		Size: 28.9 MB (28861317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f8ec3a3aaea2ec5b141647d738aebd08a3c2cbf875cc9d8fadbb153224db83a`  
		Last Modified: Thu, 18 Sep 2025 18:51:09 GMT  
		Size: 5.0 MB (4971714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07c5fcade66826ab14a0a45919cc20b012888d89c16c66f64d9502a2f317a89`  
		Last Modified: Thu, 18 Sep 2025 18:51:05 GMT  
		Size: 3.5 KB (3526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a85b7d5ef6ff0cb4f7033f24267c602efcd9274c188627595735833d79d48f`  
		Last Modified: Thu, 18 Sep 2025 18:52:58 GMT  
		Size: 504.2 MB (504155194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a799786c50fa2e3d89d5eb5915313dbd2800c12cfaf245d1611d19b3790acea`  
		Last Modified: Thu, 18 Sep 2025 18:51:05 GMT  
		Size: 9.1 KB (9104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f79ca61efb1e2c462640659610d4a1223e85d19ac817fd533a3fb2c61fad89b7`  
		Last Modified: Thu, 18 Sep 2025 18:51:05 GMT  
		Size: 1.7 KB (1715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16146084f647c3fcdfdb6e2234d5d25978ee3a85ee8da9c9702811e7f5eb79bb`  
		Last Modified: Thu, 18 Sep 2025 18:51:05 GMT  
		Size: 160.4 KB (160358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ff3702d9aa78de2e741074f2afef2a3cf97abd2716e02b2bdd649cf17807c7`  
		Last Modified: Thu, 18 Sep 2025 18:51:05 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5c7bf34d618c383c9794e8495ba0f702d91a361a27d408ffe3c930ecebd0b0e`  
		Last Modified: Thu, 18 Sep 2025 18:51:06 GMT  
		Size: 115.5 KB (115530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.19.4` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:b94ac2b91ddcf4591a50537207be1b89df774c31938f6ac628249d8aa1279e14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3251702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4f700f16d3eae18c4a80e7fd66c59ac2176d70404dd6ef306ca8896a94b3124`

```dockerfile
```

-	Layers:
	-	`sha256:cb45390f3225767c858f5af87b1be3ced2b3bfb2d81553c298b23d5f1daf6049`  
		Last Modified: Thu, 18 Sep 2025 21:25:30 GMT  
		Size: 3.2 MB (3214616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bed28de0fce04e0e2ab3a44da02610bd42339d1ae86ad769c26c2c7b9c1ddafa`  
		Last Modified: Thu, 18 Sep 2025 21:25:31 GMT  
		Size: 37.1 KB (37086 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:9.0.7`

```console
$ docker pull elasticsearch@sha256:f4867391fd4d5e2bc2ea3a9fd2ff2f5708cdc5bb77b89690fc94971bc79604e6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.0.7` - linux; amd64

```console
$ docker pull elasticsearch@sha256:6f19b3b1ed72178a53d58af887bbd82a273dd0923d36d4b352ec7ee134998a6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **700.7 MB (700687946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e44e666fb7450c1220f3e0f183a1d1df6c4b7acbc8b12592941e947a2649a1f9`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL io.openshift.expose-services=""
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 16 Sep 2025 08:32:12 GMT
ENV container oci
# Tue, 16 Sep 2025 08:32:12 GMT
COPY dir:c341d431f712f164558c0a23b4ff14b886e2ce5a998d4c5baaaa381ffd7c3b00 in / 
# Tue, 16 Sep 2025 08:32:12 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 16 Sep 2025 08:32:12 GMT
CMD ["/bin/bash"]
# Tue, 16 Sep 2025 08:32:12 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Tue, 16 Sep 2025 08:32:12 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /root/buildinfo/content_manifests/content-sets.json 
# Tue, 16 Sep 2025 08:32:12 GMT
COPY file:097ec12a5c22da979b55e75443e50150904b478d4249b64b2431aae8901ea4d2 in /root/buildinfo/labels.json 
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "org.opencontainers.image.revision"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "build-date"="2025-09-18T08:36:33Z" "release"="1758184547"
# Tue, 16 Sep 2025 08:32:12 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 16 Sep 2025 08:32:12 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 16 Sep 2025 08:32:12 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Sep 2025 08:32:12 GMT
ENV SHELL=/bin/bash
# Tue, 16 Sep 2025 08:32:12 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL org.label-schema.build-date=2025-09-10T22:06:39.784049935Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=c6d8fb31b39450a223671e79141dd1c4b2759b5f org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.0.7 org.opencontainers.image.created=2025-09-10T22:06:39.784049935Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=c6d8fb31b39450a223671e79141dd1c4b2759b5f org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.0.7
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.0.7 release=1 summary=Elasticsearch description=You know, for search.
# Tue, 16 Sep 2025 08:32:12 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 16 Sep 2025 08:32:12 GMT
CMD ["eswrapper"]
# Tue, 16 Sep 2025 08:32:12 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:9f4bff248214d12c7254dc3c25ef82bd14ff143e2a06d159f2a8cc1c9e6ef1fd`  
		Last Modified: Thu, 18 Sep 2025 15:30:42 GMT  
		Size: 39.6 MB (39648249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:921a1386559fdc3fad77d74fb02ed2865aecf66a84924c19c3e389b64bcf0004`  
		Last Modified: Fri, 19 Sep 2025 21:18:12 GMT  
		Size: 4.3 MB (4282655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac8f21a40e62169849c1353a79265ebb38aa131f0f39a036db85ff4f60730e3`  
		Last Modified: Fri, 19 Sep 2025 21:18:12 GMT  
		Size: 1.5 KB (1530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59f9d0ab21bb483ac1a1a7ea236bf5198391e3ee863f49417e0f83decddfd741`  
		Last Modified: Fri, 19 Sep 2025 21:18:14 GMT  
		Size: 9.5 KB (9532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68ac2c0ef7803bc42f70553280c374bc42163af9d822e9a36bc9b1637b03a88b`  
		Last Modified: Fri, 19 Sep 2025 21:19:16 GMT  
		Size: 656.7 MB (656666520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d68d712d0902dd8181bb529ce9c6c6e99851214e3634e490f9dc40e0633e3b97`  
		Last Modified: Fri, 19 Sep 2025 21:18:13 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d71b899601cb75af4c33ab76c01bc7bf478f78ad63fdce7aef76a7b59fa283ba`  
		Last Modified: Fri, 19 Sep 2025 21:18:14 GMT  
		Size: 1.7 KB (1718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01928d41737432ffafdb2e3e52fbd3df19b16c1cfc483e72a5c7116d4241cf3f`  
		Last Modified: Fri, 19 Sep 2025 21:18:14 GMT  
		Size: 75.7 KB (75745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0692bc25115149e5c143120bdfda15d1b49018c01a8b2c87f6e2311bb9f5f04`  
		Last Modified: Fri, 19 Sep 2025 21:18:12 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.0.7` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:a961174e11a976d37323665c2f769d606a57036bce8b648bc4a21ccb9e4bc077
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2064511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f0c0816e7a6a9c75b8ce73712ad5e150b3cb496114fe7a9aefb33e098588a55`

```dockerfile
```

-	Layers:
	-	`sha256:642e9aee8d770fd5e6b65263e50a18fe48ae33a639110bf1dd39360e7737d01c`  
		Last Modified: Fri, 19 Sep 2025 21:25:23 GMT  
		Size: 2.0 MB (2030673 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57d37b1f3fd940cfc3f5079e0fd9de8a6aab5d71846b6521b6bea19d893670ba`  
		Last Modified: Fri, 19 Sep 2025 21:25:24 GMT  
		Size: 33.8 KB (33838 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.0.7` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:6ac4fe8dacd40f955d100887e587c2cb3f1250597a256e7955f5d725c4fa98d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **539.2 MB (539213471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:379d2e7c290ccd328e9ec3708ce55544ff066bae52280b8495eaae7e28254c52`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL io.openshift.expose-services=""
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 16 Sep 2025 08:32:12 GMT
ENV container oci
# Tue, 16 Sep 2025 08:32:12 GMT
COPY dir:9f6ea5fd9a48598d911c3860918a4b145eb452cb81a81a77f69e1ed6481637df in / 
# Tue, 16 Sep 2025 08:32:12 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 16 Sep 2025 08:32:12 GMT
CMD ["/bin/bash"]
# Tue, 16 Sep 2025 08:32:12 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Tue, 16 Sep 2025 08:32:12 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /root/buildinfo/content_manifests/content-sets.json 
# Tue, 16 Sep 2025 08:32:12 GMT
COPY file:f5f06837bcbb5ebacc66d8764dd5ddb2c916d273cd4f80d9b8b34880aba3bbeb in /root/buildinfo/labels.json 
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "org.opencontainers.image.revision"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "build-date"="2025-09-18T08:39:36Z" "release"="1758184547"
# Tue, 16 Sep 2025 08:32:12 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 16 Sep 2025 08:32:12 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 16 Sep 2025 08:32:12 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Sep 2025 08:32:12 GMT
ENV SHELL=/bin/bash
# Tue, 16 Sep 2025 08:32:12 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL org.label-schema.build-date=2025-09-10T22:06:39.784049935Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=c6d8fb31b39450a223671e79141dd1c4b2759b5f org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.0.7 org.opencontainers.image.created=2025-09-10T22:06:39.784049935Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=c6d8fb31b39450a223671e79141dd1c4b2759b5f org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.0.7
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.0.7 release=1 summary=Elasticsearch description=You know, for search.
# Tue, 16 Sep 2025 08:32:12 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 16 Sep 2025 08:32:12 GMT
CMD ["eswrapper"]
# Tue, 16 Sep 2025 08:32:12 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:a9f9218e937ae927e68fe68d00604365ddda1b238616443bc0a4b9e574067342`  
		Last Modified: Thu, 18 Sep 2025 15:44:52 GMT  
		Size: 37.9 MB (37900151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b7f33888e5b67a259be391c604710b80055e9ee4740d87827669461eff488ed`  
		Last Modified: Fri, 19 Sep 2025 20:47:19 GMT  
		Size: 4.3 MB (4290411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44665faa46e15431143ad527dee58442c70b6a199f3d70fa6cfdd19555f4c3f7`  
		Last Modified: Fri, 19 Sep 2025 20:47:19 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9026ec73c64fc604d51d7ee555e0bd42289f45e46bdb8ef3d37b0235571eac26`  
		Last Modified: Fri, 19 Sep 2025 20:47:20 GMT  
		Size: 9.1 KB (9102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de94affd03766b67d7d33114e082b1680cf292cc3ecca83f12220d7cdd028c7a`  
		Last Modified: Fri, 19 Sep 2025 21:27:36 GMT  
		Size: 496.9 MB (496933925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e90d3c05d113e0894e5b0f8112e152b018d856bc631a149901b1e31f6ae6b62`  
		Last Modified: Fri, 19 Sep 2025 20:47:20 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:974c4edbe8315a6a1d1811dabe0b33f9dd7dfcbdbe80c29cd628c31278ac7074`  
		Last Modified: Fri, 19 Sep 2025 20:47:20 GMT  
		Size: 1.7 KB (1720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f3150cd8d4c07e95118b02b572152e572dd3d4ec5db419f2494e15851f65d2d`  
		Last Modified: Fri, 19 Sep 2025 20:47:20 GMT  
		Size: 74.6 KB (74638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd9e48bb4e2f3e8a74ec32d43666b1e3726846af93c3c6fb85c5005c22ce5a91`  
		Last Modified: Fri, 19 Sep 2025 20:47:21 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.0.7` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:545a8af37843a4daa1f14eddbcb39eacd7f7e471102f7c9e9a166b018e081e36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2065258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94b49bb00571f1214c9212acd2bd9eff7882e4e7f563b26dd6b79c2c699ab677`

```dockerfile
```

-	Layers:
	-	`sha256:e6e0fcfd5cfbf77751175d53d07847bdfbb971f305b5c01409a98a4ed77a9386`  
		Last Modified: Fri, 19 Sep 2025 21:25:28 GMT  
		Size: 2.0 MB (2031237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bdc2aef5686efe1720e69f0f8e10d201e36139c95552e9d830a2dd63dbf2090`  
		Last Modified: Fri, 19 Sep 2025 21:25:29 GMT  
		Size: 34.0 KB (34021 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:9.1.4`

```console
$ docker pull elasticsearch@sha256:0605584123a5e577e7da05215d80ed81473d3ad041abca686918c1295c90a549
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.1.4` - linux; amd64

```console
$ docker pull elasticsearch@sha256:9ab0d100892dd17873a683604e4105503401a918597d098ce25d2a02930d5e91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **715.7 MB (715689399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d8a06e4e4ee7c44b27bbb4690ccf9ae84b3291458b3dac99d7631c02cb423d6`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL io.openshift.expose-services=""
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 18 Sep 2025 08:05:18 GMT
ENV container oci
# Thu, 18 Sep 2025 08:05:18 GMT
COPY dir:c341d431f712f164558c0a23b4ff14b886e2ce5a998d4c5baaaa381ffd7c3b00 in / 
# Thu, 18 Sep 2025 08:05:18 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 18 Sep 2025 08:05:18 GMT
CMD ["/bin/bash"]
# Thu, 18 Sep 2025 08:05:18 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Thu, 18 Sep 2025 08:05:18 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /root/buildinfo/content_manifests/content-sets.json 
# Thu, 18 Sep 2025 08:05:18 GMT
COPY file:097ec12a5c22da979b55e75443e50150904b478d4249b64b2431aae8901ea4d2 in /root/buildinfo/labels.json 
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "org.opencontainers.image.revision"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "build-date"="2025-09-18T08:36:33Z" "release"="1758184547"
# Thu, 18 Sep 2025 08:05:18 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 18 Sep 2025 08:05:18 GMT
COPY /bin/tini /bin/tini # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 18 Sep 2025 08:05:18 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Sep 2025 08:05:18 GMT
ENV SHELL=/bin/bash
# Thu, 18 Sep 2025 08:05:18 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL org.label-schema.build-date=2025-09-16T22:05:19.073893347Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=0b7fe68d2e369469ff9e9f344ab6df64ab9c5293 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.1.4 org.opencontainers.image.created=2025-09-16T22:05:19.073893347Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=0b7fe68d2e369469ff9e9f344ab6df64ab9c5293 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.4
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.1.4 release=1 summary=Elasticsearch description=You know, for search.
# Thu, 18 Sep 2025 08:05:18 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 18 Sep 2025 08:05:18 GMT
CMD ["eswrapper"]
# Thu, 18 Sep 2025 08:05:18 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:9f4bff248214d12c7254dc3c25ef82bd14ff143e2a06d159f2a8cc1c9e6ef1fd`  
		Last Modified: Thu, 18 Sep 2025 15:30:42 GMT  
		Size: 39.6 MB (39648249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a1a049251b7bfa5ec400dc3fa47c63b05267537f7f1a41c9633f5356eb803c`  
		Last Modified: Fri, 19 Sep 2025 20:47:58 GMT  
		Size: 4.3 MB (4282663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67584a0c265f1847753e5c88807f48f0190eab56669704ac0f99b3556a1d3890`  
		Last Modified: Fri, 19 Sep 2025 20:47:58 GMT  
		Size: 1.5 KB (1531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:038fa5866cd62a62efe0dbe88b8a8b30ecf18da1ff6de0cf49e837ecf7a70eb7`  
		Last Modified: Fri, 19 Sep 2025 20:47:58 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6dc5f5c65e20827de29bc8b5e80743030409d311d09e692ab74bae724146949`  
		Last Modified: Fri, 19 Sep 2025 21:31:05 GMT  
		Size: 671.7 MB (671667958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f4e7406b96d8da6d8e4fd21b0c5bfb156b8e8092106090054197fc462a5daa`  
		Last Modified: Fri, 19 Sep 2025 20:48:01 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43d08a248b7e26b34a988dc91c69efe9882bc524952511f3a5cbbb5cfa17d271`  
		Last Modified: Fri, 19 Sep 2025 20:48:00 GMT  
		Size: 1.7 KB (1720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81cd5ffcea4cbc9ff463993762fee2d7da83652600f0d076b14af66e67a9a9e8`  
		Last Modified: Fri, 19 Sep 2025 20:48:01 GMT  
		Size: 75.8 KB (75750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da272f21b2bda95ec69a27a1cbc3d9f6d26599742edde2112a28b0d5d328b3c5`  
		Last Modified: Fri, 19 Sep 2025 20:48:01 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.1.4` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:7fd6988713d6f6159d94851faf897fd0bd5b1c29a0d85a04f76117e54bf2e920
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2118007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c70a1128f7474abd594bad5ef5e7db8f0a392f146cf2188053373483b0d29f7c`

```dockerfile
```

-	Layers:
	-	`sha256:525a02d1c3e6c21ca3801ff6bbbeb203935006bc4e69fe9c5e2385dc51dc8d41`  
		Last Modified: Fri, 19 Sep 2025 21:25:31 GMT  
		Size: 2.1 MB (2084168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc2b8e9415e0703854541acd56aeee7dd8b12bc821719be14eaf1c3676888ff0`  
		Last Modified: Fri, 19 Sep 2025 21:25:32 GMT  
		Size: 33.8 KB (33839 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.1.4` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:64d8d37090f7f755c859c2a71b5b85dfb46523b4681d405204a57db2c14f30ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **554.2 MB (554221710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:472111600f599a75eeab4e0b395922cae7fe8c37a476e53ff6f86e952a38c2f5`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL io.openshift.expose-services=""
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 18 Sep 2025 08:05:18 GMT
ENV container oci
# Thu, 18 Sep 2025 08:05:18 GMT
COPY dir:9f6ea5fd9a48598d911c3860918a4b145eb452cb81a81a77f69e1ed6481637df in / 
# Thu, 18 Sep 2025 08:05:18 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 18 Sep 2025 08:05:18 GMT
CMD ["/bin/bash"]
# Thu, 18 Sep 2025 08:05:18 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Thu, 18 Sep 2025 08:05:18 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /root/buildinfo/content_manifests/content-sets.json 
# Thu, 18 Sep 2025 08:05:18 GMT
COPY file:f5f06837bcbb5ebacc66d8764dd5ddb2c916d273cd4f80d9b8b34880aba3bbeb in /root/buildinfo/labels.json 
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "org.opencontainers.image.revision"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "build-date"="2025-09-18T08:39:36Z" "release"="1758184547"
# Thu, 18 Sep 2025 08:05:18 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 18 Sep 2025 08:05:18 GMT
COPY /bin/tini /bin/tini # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 18 Sep 2025 08:05:18 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Sep 2025 08:05:18 GMT
ENV SHELL=/bin/bash
# Thu, 18 Sep 2025 08:05:18 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL org.label-schema.build-date=2025-09-16T22:05:19.073893347Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=0b7fe68d2e369469ff9e9f344ab6df64ab9c5293 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.1.4 org.opencontainers.image.created=2025-09-16T22:05:19.073893347Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=0b7fe68d2e369469ff9e9f344ab6df64ab9c5293 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.4
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.1.4 release=1 summary=Elasticsearch description=You know, for search.
# Thu, 18 Sep 2025 08:05:18 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 18 Sep 2025 08:05:18 GMT
CMD ["eswrapper"]
# Thu, 18 Sep 2025 08:05:18 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:a9f9218e937ae927e68fe68d00604365ddda1b238616443bc0a4b9e574067342`  
		Last Modified: Thu, 18 Sep 2025 15:44:52 GMT  
		Size: 37.9 MB (37900151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf90545866d98bf757816c7957357bc6af3aff9b9881ed49577604b60b126a46`  
		Last Modified: Fri, 19 Sep 2025 20:46:50 GMT  
		Size: 4.3 MB (4290406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a538d136ff0dc21a69fc99fd813f309c3754d677fc597357999e96a121245e`  
		Last Modified: Fri, 19 Sep 2025 20:46:50 GMT  
		Size: 1.5 KB (1530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f8939d2f98f6f413ea8258b723655c5bd272944ea53024ebe8e33327488907`  
		Last Modified: Fri, 19 Sep 2025 20:46:50 GMT  
		Size: 9.1 KB (9101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6b546893a06f0a4b4e925b46e9599f7206308a0c97bee33c67ba78477051e1`  
		Last Modified: Fri, 19 Sep 2025 21:18:57 GMT  
		Size: 511.9 MB (511942164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd6f7a202c88ac0503f308f5804971d6889c02b804ff2a6f302276c2a8145558`  
		Last Modified: Fri, 19 Sep 2025 20:46:50 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da98f427c4e32c35fb03ca07d24a7dd4962af2758382759244d20f25354fbac`  
		Last Modified: Fri, 19 Sep 2025 20:46:51 GMT  
		Size: 1.7 KB (1721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc7f1906f6fa6ffb8d7822e1b2b2e363abed7fe5cc2ae9287989c437073794e`  
		Last Modified: Fri, 19 Sep 2025 20:46:51 GMT  
		Size: 74.6 KB (74640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9c1f4b224ad74619ffe45595974199eb60aeedea56fab58225613684f60315d`  
		Last Modified: Fri, 19 Sep 2025 20:46:51 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.1.4` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:4d49e663e92803971c0724b252b778f0eb0934da67591a71898e14b852170dbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2118753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10ea701c1e08ce19c3d8dcd00cb0af5629fc63d5518fbe6639f2f85eaa274b66`

```dockerfile
```

-	Layers:
	-	`sha256:088f41e56cd0625302cc63303562cb5c3665f4ad3df13a699c016be0971db6fc`  
		Last Modified: Fri, 19 Sep 2025 21:25:37 GMT  
		Size: 2.1 MB (2084732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27579a45dfe6710f32edd05a496bb0b0eb181cd3eef796cd9633d38eacb35918`  
		Last Modified: Fri, 19 Sep 2025 21:25:37 GMT  
		Size: 34.0 KB (34021 bytes)  
		MIME: application/vnd.in-toto+json
