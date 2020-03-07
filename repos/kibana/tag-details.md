<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:6.8.7`](#kibana687)
-	[`kibana:7.6.1`](#kibana761)

## `kibana:6.8.7`

```console
$ docker pull kibana@sha256:041c1e6e7556b3ecb1d492d2b0a68b80caf6d8e88b38871e672660ed6d32c9da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kibana:6.8.7` - linux; amd64

```console
$ docker pull kibana@sha256:de9651c5970c9b1b446b8ce32e358f2aee90b1eb748f50ce349d6526b9a2d84f
```

-	Docker Version: 19.03.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.2 MB (300176798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3af8016867940c8bf899cbf2fd922db26886bf9458497efd275aab91edb95998`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 12 Nov 2019 00:20:33 GMT
ADD file:45a381049c52b5664e5e911dead277b25fadbae689c0bb35be3c42dff0f2dffe in / 
# Tue, 12 Nov 2019 00:20:33 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20191001
# Tue, 12 Nov 2019 00:20:33 GMT
CMD ["/bin/bash"]
# Wed, 26 Feb 2020 15:29:32 GMT
EXPOSE 5601
# Wed, 26 Feb 2020 15:29:56 GMT
RUN yum update -y && yum install -y fontconfig freetype && yum clean all
# Wed, 26 Feb 2020 15:30:40 GMT
COPY --chown=1000:0dir:fa385d013094151d1eb4cf6d4834bb7db5fda1380b81118db85132a904d39ab6 in /usr/share/kibana 
# Wed, 26 Feb 2020 15:30:41 GMT
WORKDIR /usr/share/kibana
# Wed, 26 Feb 2020 15:30:44 GMT
RUN ln -s /usr/share/kibana /opt/kibana
# Wed, 26 Feb 2020 15:30:44 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 26 Feb 2020 15:30:44 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2020 15:30:46 GMT
COPY --chown=1000:0file:60b6181f28c99b362092ea6139b6d4112ddd0bef32d52563c33b26bdc2b51318 in /usr/share/kibana/config/kibana.yml 
# Wed, 26 Feb 2020 15:30:46 GMT
COPY --chown=1000:0file:af2bc419b515a5fca0bc857249c43a0e082e6cb60c394519993854e4bc8048ca in /usr/local/bin/ 
# Wed, 26 Feb 2020 15:30:49 GMT
RUN chmod g+ws /usr/share/kibana && find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \;
# Wed, 26 Feb 2020 15:30:52 GMT
RUN groupadd --gid 1000 kibana && useradd --uid 1000 --gid 1000 --home-dir /usr/share/kibana --no-create-home kibana
# Wed, 26 Feb 2020 15:30:52 GMT
USER kibana
# Wed, 26 Feb 2020 15:30:53 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.label-schema.name=kibana org.label-schema.version=6.8.7 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.license=Elastic License license=Elastic License
# Wed, 26 Feb 2020 15:30:53 GMT
CMD ["/usr/local/bin/kibana-docker"]
```

-	Layers:
	-	`sha256:ab5ef0e5819490abe86106fd9f4381123e37a03e80e650be39f7938d30ecb530`  
		Last Modified: Tue, 12 Nov 2019 00:23:38 GMT  
		Size: 75.8 MB (75780712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb0869a78b0b5d1f38a8138d13d0b51c21d05a2697644eb1aec3ea6659b2f07`  
		Last Modified: Wed, 04 Mar 2020 22:12:41 GMT  
		Size: 33.6 MB (33573529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59892ed7aac286085a589c865e1fd918b0b83c8898acbb63d6513df0dbc5617f`  
		Last Modified: Wed, 04 Mar 2020 22:13:05 GMT  
		Size: 190.8 MB (190817743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e5f941e2b1203ec7b9d80ca7f20fdff5678f53471414904cfe8991f3da5c99c`  
		Last Modified: Wed, 04 Mar 2020 22:12:32 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:114aba56b44ec634270269cd826da39b7bb4d096c64801e6e050876892cc95ad`  
		Last Modified: Wed, 04 Mar 2020 22:12:32 GMT  
		Size: 403.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f68e8719f8de3b8be44d3a05511824ef21c1beb8db1f033acce335774774303`  
		Last Modified: Wed, 04 Mar 2020 22:12:32 GMT  
		Size: 2.3 KB (2257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be54f167f1a03a12b72014e0fb218babc01d0751181250d3d0a445c881314b77`  
		Last Modified: Wed, 04 Mar 2020 22:12:32 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2167a6d49739a34a4f58c84d86b43177637cc78e03f595fdf51da66aa363afc`  
		Last Modified: Wed, 04 Mar 2020 22:12:32 GMT  
		Size: 1.8 KB (1849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kibana:7.6.1`

```console
$ docker pull kibana@sha256:6e707f84053b6447f82290eb08433a8d487263aef4b4800bd72cdec362dc216d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kibana:7.6.1` - linux; amd64

```console
$ docker pull kibana@sha256:4baf80345b2bd2e6dfdf6b707cbfdf78b1be04000f758da3726b8f95a1096cc6
```

-	Docker Version: 19.03.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.3 MB (361291275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9ca33465ce347f60dc560c30da51500cc8f61321206f665f763f0bb40098045`
-	Entrypoint: `["\/usr\/local\/bin\/dumb-init","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 12 Nov 2019 00:20:33 GMT
ADD file:45a381049c52b5664e5e911dead277b25fadbae689c0bb35be3c42dff0f2dffe in / 
# Tue, 12 Nov 2019 00:20:33 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20191001
# Tue, 12 Nov 2019 00:20:33 GMT
CMD ["/bin/bash"]
# Sat, 29 Feb 2020 01:08:39 GMT
EXPOSE 5601
# Sat, 29 Feb 2020 01:09:17 GMT
RUN yum update -y && yum install -y fontconfig freetype shadow-utils && yum clean all
# Sat, 29 Feb 2020 01:09:18 GMT
RUN curl -L -o /usr/local/bin/dumb-init https://github.com/Yelp/dumb-init/releases/download/v1.2.2/dumb-init_1.2.2_amd64
# Sat, 29 Feb 2020 01:09:19 GMT
RUN echo "37f2c1f0372a45554f1b89924fbb134fc24c3756efaedf11e07f599494e0eff9  /usr/local/bin/dumb-init" | sha256sum -c -
# Sat, 29 Feb 2020 01:09:19 GMT
RUN chmod +x /usr/local/bin/dumb-init
# Sat, 29 Feb 2020 01:10:06 GMT
COPY --chown=1000:0dir:f9476d8ba38c42dc80b29804e4126e1d8137731e10366d894ec886ef7c9794ed in /usr/share/kibana 
# Sat, 29 Feb 2020 01:10:08 GMT
WORKDIR /usr/share/kibana
# Sat, 29 Feb 2020 01:10:09 GMT
RUN ln -s /usr/share/kibana /opt/kibana
# Sat, 29 Feb 2020 01:10:09 GMT
ENV ELASTIC_CONTAINER=true
# Sat, 29 Feb 2020 01:10:09 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 29 Feb 2020 01:10:10 GMT
COPY --chown=1000:0file:60b6181f28c99b362092ea6139b6d4112ddd0bef32d52563c33b26bdc2b51318 in /usr/share/kibana/config/kibana.yml 
# Sat, 29 Feb 2020 01:10:10 GMT
COPY --chown=1000:0file:0d24c5e38b0b17ceeb1508e02edbf4be9a750e9c5fa6853e5f9cbed55c4b17d2 in /usr/local/bin/ 
# Sat, 29 Feb 2020 01:10:11 GMT
RUN chmod g+ws /usr/share/kibana && find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \;
# Sat, 29 Feb 2020 01:10:12 GMT
RUN groupadd --gid 1000 kibana && useradd --uid 1000 --gid 1000 --home-dir /usr/share/kibana --no-create-home kibana
# Sat, 29 Feb 2020 01:10:12 GMT
USER kibana
# Sat, 29 Feb 2020 01:10:12 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.label-schema.name=kibana org.label-schema.version=7.6.1 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.license=Elastic License org.label-schema.usage=https://www.elastic.co/guide/en/kibana/index.html org.label-schema.build-date=2020-02-29T01:05:44.941Z license=Elastic License
# Sat, 29 Feb 2020 01:10:12 GMT
ENTRYPOINT ["/usr/local/bin/dumb-init" "--"]
# Sat, 29 Feb 2020 01:10:13 GMT
CMD ["/usr/local/bin/kibana-docker"]
```

-	Layers:
	-	`sha256:ab5ef0e5819490abe86106fd9f4381123e37a03e80e650be39f7938d30ecb530`  
		Last Modified: Tue, 12 Nov 2019 00:23:38 GMT  
		Size: 75.8 MB (75780712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4688aece0e6317d5eabe68ef1fedb5782ff47f01432f93494e132ed144473d02`  
		Last Modified: Wed, 04 Mar 2020 21:10:39 GMT  
		Size: 33.6 MB (33577555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10367b8080e4eb65a73ec6416cd17468400cca46351eea6be6139b53011fad4b`  
		Last Modified: Wed, 04 Mar 2020 21:10:26 GMT  
		Size: 31.7 KB (31695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a7fc3327f9831c5ac9207281fb669ed8f41ab8714b539e6e3b644a3fb942ba4`  
		Last Modified: Wed, 04 Mar 2020 21:10:27 GMT  
		Size: 30.2 KB (30206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f9fc05132ce5dd46af69963b4c6084c23269a30680c65a6211b5972f98a9a93`  
		Last Modified: Wed, 04 Mar 2020 22:14:45 GMT  
		Size: 251.9 MB (251865591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1656961b5569721b5d379f1a3e1c359ada166553616d910076412bf526346002`  
		Last Modified: Wed, 04 Mar 2020 22:13:53 GMT  
		Size: 140.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb98bb05a208bdc00d892cdee440d0006e85cad4135e0dc95138f905cac14bf`  
		Last Modified: Wed, 04 Mar 2020 22:13:52 GMT  
		Size: 403.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9383df8d70220eec3d3b48cef69da5ab7086ad8e0f9d9e215ae74b0235dcd495`  
		Last Modified: Wed, 04 Mar 2020 22:13:52 GMT  
		Size: 3.0 KB (2958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e3b165babc82222acd1a9acd5e03e9dd3a71785c8495f81003318c7d6b37f8d`  
		Last Modified: Wed, 04 Mar 2020 22:13:52 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:069d64f8ecc384892f5e862485a772db945fe43d9b123d11ed16bc5692786fa7`  
		Last Modified: Wed, 04 Mar 2020 22:13:53 GMT  
		Size: 1.8 KB (1849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
