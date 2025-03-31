<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `nats`

-	[`nats:2`](#nats2)
-	[`nats:2-alpine`](#nats2-alpine)
-	[`nats:2-alpine3.21`](#nats2-alpine321)
-	[`nats:2-linux`](#nats2-linux)
-	[`nats:2-nanoserver`](#nats2-nanoserver)
-	[`nats:2-nanoserver-1809`](#nats2-nanoserver-1809)
-	[`nats:2-scratch`](#nats2-scratch)
-	[`nats:2-windowsservercore`](#nats2-windowsservercore)
-	[`nats:2-windowsservercore-1809`](#nats2-windowsservercore-1809)
-	[`nats:2.10`](#nats210)
-	[`nats:2.10-alpine`](#nats210-alpine)
-	[`nats:2.10-alpine3.21`](#nats210-alpine321)
-	[`nats:2.10-linux`](#nats210-linux)
-	[`nats:2.10-nanoserver`](#nats210-nanoserver)
-	[`nats:2.10-nanoserver-1809`](#nats210-nanoserver-1809)
-	[`nats:2.10-scratch`](#nats210-scratch)
-	[`nats:2.10-windowsservercore`](#nats210-windowsservercore)
-	[`nats:2.10-windowsservercore-1809`](#nats210-windowsservercore-1809)
-	[`nats:2.10.27-binary`](#nats21027-binary)
-	[`nats:2.10.27-binary-alpine`](#nats21027-binary-alpine)
-	[`nats:2.10.27-binary-alpine3.21`](#nats21027-binary-alpine321)
-	[`nats:2.10.27-binary-linux`](#nats21027-binary-linux)
-	[`nats:2.10.27-binary-nanoserver`](#nats21027-binary-nanoserver)
-	[`nats:2.10.27-binary-nanoserver-1809`](#nats21027-binary-nanoserver-1809)
-	[`nats:2.10.27-binary-scratch`](#nats21027-binary-scratch)
-	[`nats:2.10.27-binary-windowsservercore`](#nats21027-binary-windowsservercore)
-	[`nats:2.10.27-binary-windowsservercore-1809`](#nats21027-binary-windowsservercore-1809)
-	[`nats:2.11`](#nats211)
-	[`nats:2.11-alpine`](#nats211-alpine)
-	[`nats:2.11-alpine3.21`](#nats211-alpine321)
-	[`nats:2.11-linux`](#nats211-linux)
-	[`nats:2.11-nanoserver`](#nats211-nanoserver)
-	[`nats:2.11-nanoserver-1809`](#nats211-nanoserver-1809)
-	[`nats:2.11-scratch`](#nats211-scratch)
-	[`nats:2.11-windowsservercore`](#nats211-windowsservercore)
-	[`nats:2.11-windowsservercore-1809`](#nats211-windowsservercore-1809)
-	[`nats:2.11.1-binary`](#nats2111-binary)
-	[`nats:2.11.1-binary-alpine`](#nats2111-binary-alpine)
-	[`nats:2.11.1-binary-alpine3.21`](#nats2111-binary-alpine321)
-	[`nats:2.11.1-binary-linux`](#nats2111-binary-linux)
-	[`nats:2.11.1-binary-nanoserver`](#nats2111-binary-nanoserver)
-	[`nats:2.11.1-binary-nanoserver-1809`](#nats2111-binary-nanoserver-1809)
-	[`nats:2.11.1-binary-scratch`](#nats2111-binary-scratch)
-	[`nats:2.11.1-binary-windowsservercore`](#nats2111-binary-windowsservercore)
-	[`nats:2.11.1-binary-windowsservercore-1809`](#nats2111-binary-windowsservercore-1809)
-	[`nats:alpine`](#natsalpine)
-	[`nats:alpine3.21`](#natsalpine321)
-	[`nats:latest`](#natslatest)
-	[`nats:linux`](#natslinux)
-	[`nats:nanoserver`](#natsnanoserver)
-	[`nats:nanoserver-1809`](#natsnanoserver-1809)
-	[`nats:scratch`](#natsscratch)
-	[`nats:windowsservercore`](#natswindowsservercore)
-	[`nats:windowsservercore-1809`](#natswindowsservercore-1809)

## `nats:2`

```console
$ docker pull nats@sha256:76fe53997736051e3511ddc26d585abd679fe3a30dbf74d19418bb0035fde031
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 13
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown
	-	windows version 10.0.17763.7009; amd64

### `nats:2` - linux; amd64

```console
$ docker pull nats@sha256:0b313c16824b8d98736c06153fa01af3c8d62eebc6298e9062fd2e00c0a3e865
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6282666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5a2333da61b6c9f0de1de8235aca52ee071283b0c8c6487d3ea15b4a0f9f8e2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:54120e60f5a574cbbfd83de2711330ae98499a27ff592bdb694994b87749dd23`  
		Last Modified: Mon, 31 Mar 2025 17:41:30 GMT  
		Size: 6.3 MB (6282155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71d71c31c70e45e814d8db85102321f1459be653c595cd91fafb76306cdf405e`  
		Last Modified: Mon, 31 Mar 2025 19:07:36 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:b8d62bc797363d5eab76aea96ec144d02b901da4dba8eb8bf31cc4e51e3a09d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbd51cd5b25ea5c4355cd2cde0e286d4f6da98802af9ed8b477001ff7ece4679`

```dockerfile
```

-	Layers:
	-	`sha256:19abc39a4cbb247bfa12363ce59bbce1e3bf861fddb9055c3a17e2d39d54d204`  
		Last Modified: Mon, 31 Mar 2025 19:07:36 GMT  
		Size: 10.5 KB (10523 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; arm variant v6

```console
$ docker pull nats@sha256:af5758489c2981e0a1028dc47f82f0dd2d26e2fac7ac1e478a2a15a12029f6d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6002169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c17f13cf88d7cb6d029eafd34cd847cbacebb2131dc5b7ecfbed791e2958e6a4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:098bda892a4e7ddd77ca838f72ef9757e9b3cfae3c7bc97076a8dd0b6fd92597`  
		Last Modified: Mon, 31 Mar 2025 17:41:30 GMT  
		Size: 6.0 MB (6001660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff1d2651842734b21329c25e1004a4da19102e57001381e60bb4fd58723fe19`  
		Last Modified: Mon, 31 Mar 2025 19:07:08 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:736b8ee8472809de9731d9c426d2113e533e5ac68c9fbf4cd6bb44eb636b3d79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ffa52afcf9f827961f6f692daeb94f398721ac7559f559d56147558f6742150`

```dockerfile
```

-	Layers:
	-	`sha256:cc5887e8b88d73925b5364f9143ca37566f003a1560dffe173f7be8f10d66806`  
		Last Modified: Mon, 31 Mar 2025 19:07:08 GMT  
		Size: 10.7 KB (10650 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; arm variant v7

```console
$ docker pull nats@sha256:f1752b6d8b3a5506fab1fdf93ce66a6bd6e934d33a3c230231458f254ff505a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5992492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68d3d700cbec0d68868397c08f331e9cee8a3e484035ab651de2414c1bc1039b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7ae07ef7aadc186e26516a3b1a5bacd27b42c41b8d63efc540622587ef29be07`  
		Last Modified: Mon, 31 Mar 2025 17:41:36 GMT  
		Size: 6.0 MB (5991983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d132fb7bc19f6f368e535b5a46903e88d661e5c0f5e33c79b7d66b962039598`  
		Last Modified: Mon, 31 Mar 2025 20:44:23 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:ff00ada993e928a0dbcd0e627e845b5f9c4d11042f0e089912b8ef2969c89876
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab26b373d46f30d56fc9b9ecf02d3c518eb5ab041a8fbb69e562b49b1a864d9d`

```dockerfile
```

-	Layers:
	-	`sha256:d552b4d64ce37965149a8aaeed3a0eebd251066efc77cb63ad2307f9d0bbdef7`  
		Last Modified: Mon, 31 Mar 2025 20:44:23 GMT  
		Size: 10.6 KB (10649 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a360fbbfeb6f19012e875675cf70ea15e5ea3d9e003d5ccf1a61adeed8d515c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5776951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aad8d86003a865c09c995830bd52c9154c44e7976be35a0790b217a28445c6c2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:813138f2f23c3f67c00cc3f899e890b4b46ad187b3c70730ab91bd63ff37fa6d`  
		Last Modified: Mon, 31 Mar 2025 17:41:30 GMT  
		Size: 5.8 MB (5776442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d132fb7bc19f6f368e535b5a46903e88d661e5c0f5e33c79b7d66b962039598`  
		Last Modified: Mon, 31 Mar 2025 20:44:23 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:13fe1989809a4185209660bba2e8a407b921e80a959889e94c8d6b18e6eadc66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cebd7eb7627ea55d24e6c1b36e5124796e00e1a2243414d5b3f65ff44089ec66`

```dockerfile
```

-	Layers:
	-	`sha256:a33f391d8364f479953478aa1b1ce3f8e6e05c31407e5d9ead5d4d5db6da559f`  
		Last Modified: Mon, 31 Mar 2025 20:44:29 GMT  
		Size: 10.7 KB (10708 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; ppc64le

```console
$ docker pull nats@sha256:74e2df57ac704452ee531238216b3accd76025199ee310563732dd2c680227a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5757216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abd71cf45edbcaea354422b03a686d602fac79be9357fdbc6b5c05d8ab8309e5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:452917a8c6e0add88a19efed21ff3bf850d722622f476c3b9d4426f3dbaaffb7`  
		Last Modified: Mon, 31 Mar 2025 17:41:27 GMT  
		Size: 5.8 MB (5756706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc09a85b63b7a6867f196c8c27905ad711a7457fa91d3df80022bc3d24111b3`  
		Last Modified: Mon, 31 Mar 2025 20:07:44 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:9460476db24c3ccd45c6374ab5e0dfa8af2b95e6ed003b294fca69a3f6d49e72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8048c19445dcae5f87494cedbc4822265fb6848963d3958920bc8a77dc19881`

```dockerfile
```

-	Layers:
	-	`sha256:2e79f43f61fe3cbbfb9fa2ab55acbd3a3254d4378c81f4bef4392b1b18e91f10`  
		Last Modified: Mon, 31 Mar 2025 20:07:44 GMT  
		Size: 10.6 KB (10613 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; s390x

```console
$ docker pull nats@sha256:6b9323c60c161cbd82daa5b02f46e55051f8540e7c9770dc1c2ed619086c6f53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6122555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb48b95165c0163d0de0d793f09fa9aaa8dbc79c4b50241ee9e33ac819b1a501`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:cdb5d3b73d4e5760c377e2d1a31f668fd95251ac45157f6a4c4d98139b337e23`  
		Last Modified: Mon, 31 Mar 2025 17:41:31 GMT  
		Size: 6.1 MB (6122046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16e9431fd0e418054b688573b0ef6c205ce09bcb9015c474b01a32d6800912d0`  
		Last Modified: Mon, 31 Mar 2025 20:07:36 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:2dfb1482f9d33c4a0f01a77e40b206f5b997b290b5e3899ee0c2678dd35731a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff58880fe981b8b31c473e8e992460d1ef7a218db9dd4ffc3a951750055bfd3`

```dockerfile
```

-	Layers:
	-	`sha256:9bb52fda18a732bf8f1ead6cd17dd200cfcae43fd84710a4ddb71372c0815f2b`  
		Last Modified: Mon, 31 Mar 2025 20:07:36 GMT  
		Size: 10.5 KB (10523 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - windows version 10.0.17763.7009; amd64

```console
$ docker pull nats@sha256:7523855e64c122a386122c97e7e122f78929c93ef1aaeabcfb818f96108eb526
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.4 MB (113369799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59c769ae1c19e869c3ab50a8bcc53b7a416139faa1f967bef29391891ff94a43`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 05 Mar 2025 21:54:26 GMT
RUN Apply image 10.0.17763.7009
# Mon, 31 Mar 2025 19:16:51 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Mon, 31 Mar 2025 19:16:54 GMT
RUN cmd /S /C #(nop) COPY file:cbd316e46d1e3baa5a0ffb6e227be5b521aa07a7cbe3a0513c0076ac28429bf3 in C:\nats-server.exe 
# Mon, 31 Mar 2025 19:16:55 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Mon, 31 Mar 2025 19:16:55 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Mon, 31 Mar 2025 19:16:56 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 31 Mar 2025 19:16:56 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:543388a101bf4d470af7e8817eff3f6f3b98f13d106939ab3f507a28f2825d0a`  
		Last Modified: Tue, 11 Mar 2025 22:40:48 GMT  
		Size: 106.9 MB (106907688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5764592bce5a260f59c0fc8af513aa702c03e73d61b9d9769cfb463cb5d345a4`  
		Last Modified: Mon, 31 Mar 2025 19:17:00 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c220ae7f5568ad8b19e77200fe2ab8b43bd7e66c8215b73f18cab048bf4c949b`  
		Last Modified: Mon, 31 Mar 2025 19:16:59 GMT  
		Size: 6.5 MB (6456094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24b9abd521fc3bf26173541357dca364e2aaa425fa95150aa12063ad86adbd0f`  
		Last Modified: Mon, 31 Mar 2025 19:16:59 GMT  
		Size: 1.7 KB (1684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47263123c2dca13a6ccd5e6c3f836df870102b1186585b3533a50841169f2d5d`  
		Last Modified: Mon, 31 Mar 2025 19:16:59 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb4c62df8bd6d5f27aca099be80d7290759022e9ed845409d9608b11f0e3db16`  
		Last Modified: Mon, 31 Mar 2025 19:16:58 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faf623903ff066d1e92e2c9250d8f7cd5a3230c1ea39d9cbe269fd63e735f4be`  
		Last Modified: Mon, 31 Mar 2025 19:16:59 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine`

```console
$ docker pull nats@sha256:222b8a7f2b9cbef1a51d412a5782ee75eac04062413d61c960b051e29c214115
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2-alpine` - linux; amd64

```console
$ docker pull nats@sha256:d2bfc2b0b53f2a35c4b1c6fb432695b13dd232bdb551ea62c9fc00148520401f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10386128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6a871a4d4c93dc7e032ef72a3a722439e2ce32e96063585474891c6b654043f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
ENV NATS_SERVER=2.11.1-binary
# Mon, 31 Mar 2025 17:39:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='2499105f9e64bef55f168f634d34a586b710f6ac041639d8a18364f2b4f4c410' ;; 		armhf) natsArch='arm6'; sha256='31bc11906458e30c8028cdd0301de98713074db73f5e352f58ce4ecd6b1cc641' ;; 		armv7) natsArch='arm7'; sha256='432f4c47cf5adca05da67f1feaf969f6cea50ed9c3bb743a8bb76b8c5c583c8e' ;; 		x86_64) natsArch='amd64'; sha256='827497f99acd54eb0e4e8bfa3b0eb31dd51c6c259110de11a45a7fdacae6c5b3' ;; 		x86) natsArch='386'; sha256='651065e2170ee0f7e244425c0d0ba30a38776a7aef75e2d5cba0b8b11a950c54' ;; 		s390x) natsArch='s390x'; sha256='23e6ce6b70f9b973106d325eebb8bdd613040bedd4da980ff0aea2d2a7dc122e' ;; 		ppc64le) natsArch='ppc64le'; sha256='5341f41ef6298b05b72dd77c1ec055aeacb1b57dfd600ec888317347b3b4cbf8' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0643a146757fce88425f18db35388da5f1441b9e655395106fc3b6de8f7779a`  
		Last Modified: Mon, 31 Mar 2025 18:43:34 GMT  
		Size: 6.7 MB (6742912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f810863f848d47b0ec90164d81013c3f49b7d5d94bf9c42a73558dc7c46cfce`  
		Last Modified: Mon, 31 Mar 2025 18:43:33 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3295cd3199e071474b886bbbcf41ef4c12302ddbe5f1bd9283c8e119abcefe39`  
		Last Modified: Mon, 31 Mar 2025 18:43:33 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:7a817ee3d7045d87d4f49299e408201d1118ee221fdda63c5b66733871a32dea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89e54e9039e9d3c99605b12728bbecef9c9479593bdf67a68e894df9ecba60c4`

```dockerfile
```

-	Layers:
	-	`sha256:d380a2bbbdfb0718224f60b142dc29624483f0d28fa0552fb8e915ab9c1d69d2`  
		Last Modified: Mon, 31 Mar 2025 18:43:33 GMT  
		Size: 14.4 KB (14360 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:5b003eca587d5d1ded87d52f52a88b49c6091e2ae6ffcbcc9591ef31edfb1153
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9830711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd78fe0bc28317f1acadcd3ed9a09443a843f5cf68ef058de361ff0570543e01`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
ENV NATS_SERVER=2.11.1-binary
# Mon, 31 Mar 2025 17:39:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='2499105f9e64bef55f168f634d34a586b710f6ac041639d8a18364f2b4f4c410' ;; 		armhf) natsArch='arm6'; sha256='31bc11906458e30c8028cdd0301de98713074db73f5e352f58ce4ecd6b1cc641' ;; 		armv7) natsArch='arm7'; sha256='432f4c47cf5adca05da67f1feaf969f6cea50ed9c3bb743a8bb76b8c5c583c8e' ;; 		x86_64) natsArch='amd64'; sha256='827497f99acd54eb0e4e8bfa3b0eb31dd51c6c259110de11a45a7fdacae6c5b3' ;; 		x86) natsArch='386'; sha256='651065e2170ee0f7e244425c0d0ba30a38776a7aef75e2d5cba0b8b11a950c54' ;; 		s390x) natsArch='s390x'; sha256='23e6ce6b70f9b973106d325eebb8bdd613040bedd4da980ff0aea2d2a7dc122e' ;; 		ppc64le) natsArch='ppc64le'; sha256='5341f41ef6298b05b72dd77c1ec055aeacb1b57dfd600ec888317347b3b4cbf8' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c92f9bdc82b0d8955653988d31a42d2d808133d9b313a6f16c7c1fc6187ce7c3`  
		Last Modified: Mon, 31 Mar 2025 18:50:14 GMT  
		Size: 6.5 MB (6465008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f8f3e30080f28fb154a8574bfa9e68094196baa500cc70232b4b6a993d7d96`  
		Last Modified: Mon, 31 Mar 2025 18:50:13 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b07ed84ffecb4fe35014c6ec28f044236b811f87738a6e32d50061b6cdcf8913`  
		Last Modified: Mon, 31 Mar 2025 18:50:13 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:25ca21f30fda2b87f68ede801458791fdf7fb7571b1dfc4c5b92a80f7287b667
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fa2e55e1097547a0c5dc17d479d5b338734fce9c9e83240bf6a9eb19569188a`

```dockerfile
```

-	Layers:
	-	`sha256:f659982640e897f8f52e71b1b320e9ea56d5354063a38cf666928fe3ccf97400`  
		Last Modified: Mon, 31 Mar 2025 18:50:13 GMT  
		Size: 14.5 KB (14468 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:f6f902d9d220b13f8c52befb0e4f2520a530e999e9d0d7e3b4a7c96d1d6a2d4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9552225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f49a7e1e59161babacc6a62e07238abd7b349a8efc80a4bfd1523785ae8ece72`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
ENV NATS_SERVER=2.11.1-binary
# Mon, 31 Mar 2025 17:39:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='2499105f9e64bef55f168f634d34a586b710f6ac041639d8a18364f2b4f4c410' ;; 		armhf) natsArch='arm6'; sha256='31bc11906458e30c8028cdd0301de98713074db73f5e352f58ce4ecd6b1cc641' ;; 		armv7) natsArch='arm7'; sha256='432f4c47cf5adca05da67f1feaf969f6cea50ed9c3bb743a8bb76b8c5c583c8e' ;; 		x86_64) natsArch='amd64'; sha256='827497f99acd54eb0e4e8bfa3b0eb31dd51c6c259110de11a45a7fdacae6c5b3' ;; 		x86) natsArch='386'; sha256='651065e2170ee0f7e244425c0d0ba30a38776a7aef75e2d5cba0b8b11a950c54' ;; 		s390x) natsArch='s390x'; sha256='23e6ce6b70f9b973106d325eebb8bdd613040bedd4da980ff0aea2d2a7dc122e' ;; 		ppc64le) natsArch='ppc64le'; sha256='5341f41ef6298b05b72dd77c1ec055aeacb1b57dfd600ec888317347b3b4cbf8' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4be7f6d278a4174ef17dcd8c89848f067134976f430004cbed069643b89e46e8`  
		Last Modified: Mon, 31 Mar 2025 20:17:05 GMT  
		Size: 6.5 MB (6453133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825c724725f466486a81cdde1ec6a92840eb03f19fc7c9f6c2361d13f3398293`  
		Last Modified: Mon, 31 Mar 2025 20:17:04 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe87685444a72475e87e5ffbb1baff8c65017859e8e53c72573fc546273e8ef6`  
		Last Modified: Mon, 31 Mar 2025 20:17:04 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:860dd6d0c495dc91deb8a4c27e98247c01e7cc5ba0a4a80d0e33430aaa5695db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41756094504db64ff2b19360c941882401645db6e11cb7b116c9cc5d965c1002`

```dockerfile
```

-	Layers:
	-	`sha256:a83dd1e9193bcbd50a20cfab9ac07e63cb0d3f71b71000fc9b9e4456a63ddc2c`  
		Last Modified: Mon, 31 Mar 2025 20:17:04 GMT  
		Size: 14.5 KB (14468 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:90874ce66332c5ed35925509121cc1231be38266af7f5efe7097f37a54610dc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10234990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e934c9514dbf2966156ca2a5b60a8c62eab86a1d0e9316d96e587bc52837aff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
ENV NATS_SERVER=2.11.1-binary
# Mon, 31 Mar 2025 17:39:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='2499105f9e64bef55f168f634d34a586b710f6ac041639d8a18364f2b4f4c410' ;; 		armhf) natsArch='arm6'; sha256='31bc11906458e30c8028cdd0301de98713074db73f5e352f58ce4ecd6b1cc641' ;; 		armv7) natsArch='arm7'; sha256='432f4c47cf5adca05da67f1feaf969f6cea50ed9c3bb743a8bb76b8c5c583c8e' ;; 		x86_64) natsArch='amd64'; sha256='827497f99acd54eb0e4e8bfa3b0eb31dd51c6c259110de11a45a7fdacae6c5b3' ;; 		x86) natsArch='386'; sha256='651065e2170ee0f7e244425c0d0ba30a38776a7aef75e2d5cba0b8b11a950c54' ;; 		s390x) natsArch='s390x'; sha256='23e6ce6b70f9b973106d325eebb8bdd613040bedd4da980ff0aea2d2a7dc122e' ;; 		ppc64le) natsArch='ppc64le'; sha256='5341f41ef6298b05b72dd77c1ec055aeacb1b57dfd600ec888317347b3b4cbf8' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60797fdb0b4d910be869065ae81ab51200fbe5544785eb4efa8fc7cb9eb3033e`  
		Last Modified: Mon, 31 Mar 2025 20:11:13 GMT  
		Size: 6.2 MB (6240991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dda5bbcac3d56d1f2414331f89b9333ef3393083b91ce07a2face8802428335`  
		Last Modified: Mon, 31 Mar 2025 20:11:12 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c42e24e15c065a92a28be68d337a0e3f21fc9b4bee9e5e931179ab16a647031`  
		Last Modified: Mon, 31 Mar 2025 20:11:12 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:061fa681d240f27b08e83d14d855bff8191035c3944adf647afab28af9d67b5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a76bc64a67b68410441588e0e8ebc82c70ec9260099bfb6d4d5154152785d62`

```dockerfile
```

-	Layers:
	-	`sha256:5b3a7763692c9fffeebb31f53b8a14d7192250292c1661653d8912d27e67bd34`  
		Last Modified: Mon, 31 Mar 2025 20:11:12 GMT  
		Size: 14.5 KB (14512 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:f09b96d5bfacda0649814f91facba68b0ecca96de4ebdea7e17dfde79f1ada96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9796685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10c6bb2aed5161b870f53898cce57635999f3e6368d89209be712832cb7caae3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
ENV NATS_SERVER=2.11.1-binary
# Mon, 31 Mar 2025 17:39:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='2499105f9e64bef55f168f634d34a586b710f6ac041639d8a18364f2b4f4c410' ;; 		armhf) natsArch='arm6'; sha256='31bc11906458e30c8028cdd0301de98713074db73f5e352f58ce4ecd6b1cc641' ;; 		armv7) natsArch='arm7'; sha256='432f4c47cf5adca05da67f1feaf969f6cea50ed9c3bb743a8bb76b8c5c583c8e' ;; 		x86_64) natsArch='amd64'; sha256='827497f99acd54eb0e4e8bfa3b0eb31dd51c6c259110de11a45a7fdacae6c5b3' ;; 		x86) natsArch='386'; sha256='651065e2170ee0f7e244425c0d0ba30a38776a7aef75e2d5cba0b8b11a950c54' ;; 		s390x) natsArch='s390x'; sha256='23e6ce6b70f9b973106d325eebb8bdd613040bedd4da980ff0aea2d2a7dc122e' ;; 		ppc64le) natsArch='ppc64le'; sha256='5341f41ef6298b05b72dd77c1ec055aeacb1b57dfd600ec888317347b3b4cbf8' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:299c0ee564e4568e71d43a566874e9d853458071d554386ad5728913e55f5d42`  
		Last Modified: Mon, 31 Mar 2025 19:45:06 GMT  
		Size: 6.2 MB (6221370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1af98871a1453d715b201d0cb6c30c2e8240dd12ee7af67f4334bfb80877f3bb`  
		Last Modified: Mon, 31 Mar 2025 19:45:05 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:103d308786c4f17ef7f21746eadc69443e28518b33fd5534040a513bbb5acc64`  
		Last Modified: Mon, 31 Mar 2025 19:45:05 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:261ca6909da20cd9b36804c44211d5a257a4f0a8746e425a8d63cebe1ff274eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bf43f070134532bf9419111138ee6504a3b9010b90d59e6380375b5b9a4abcf`

```dockerfile
```

-	Layers:
	-	`sha256:09877c6dec89674d2ec4aefc8edd75ff573a4834ca2851e1a4be89994ffcd528`  
		Last Modified: Mon, 31 Mar 2025 19:45:05 GMT  
		Size: 14.4 KB (14427 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; s390x

```console
$ docker pull nats@sha256:c14e89986785ed37ac2931d4b307ea84375f49180341e48c9024fe40f226decc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10053962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:893690471f61ea43e10126b7ceb4fd7a07fd98eb86fff95edc6cd8cf10d1e4ef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
ENV NATS_SERVER=2.11.1-binary
# Mon, 31 Mar 2025 17:39:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='2499105f9e64bef55f168f634d34a586b710f6ac041639d8a18364f2b4f4c410' ;; 		armhf) natsArch='arm6'; sha256='31bc11906458e30c8028cdd0301de98713074db73f5e352f58ce4ecd6b1cc641' ;; 		armv7) natsArch='arm7'; sha256='432f4c47cf5adca05da67f1feaf969f6cea50ed9c3bb743a8bb76b8c5c583c8e' ;; 		x86_64) natsArch='amd64'; sha256='827497f99acd54eb0e4e8bfa3b0eb31dd51c6c259110de11a45a7fdacae6c5b3' ;; 		x86) natsArch='386'; sha256='651065e2170ee0f7e244425c0d0ba30a38776a7aef75e2d5cba0b8b11a950c54' ;; 		s390x) natsArch='s390x'; sha256='23e6ce6b70f9b973106d325eebb8bdd613040bedd4da980ff0aea2d2a7dc122e' ;; 		ppc64le) natsArch='ppc64le'; sha256='5341f41ef6298b05b72dd77c1ec055aeacb1b57dfd600ec888317347b3b4cbf8' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67f000d40cf6813dabcb134d2a9b15f3b7eb5ba7dba583ad1df023b35efd9ca`  
		Last Modified: Mon, 31 Mar 2025 19:28:46 GMT  
		Size: 6.6 MB (6585424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4501a9ec92d7d9a89fd0e10cd2ba4c8fb93658a4d46301543d45d1f96b07ce32`  
		Last Modified: Mon, 31 Mar 2025 19:28:45 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06c2b65e72a2a266d2d783396559cd0ee8346a11e25f65ca2b21cc82de4174b6`  
		Last Modified: Mon, 31 Mar 2025 19:28:45 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:82ec15847478c49a8a561d7f21d2239bbea2614e277659456213e6bdd0f5dd49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:443d1aa445d5406aada9c0970885e837d983ea976af12760bad0de2704481f16`

```dockerfile
```

-	Layers:
	-	`sha256:688e4b2d5f0fdef107c3405864e3c9cc14ae13fd320ceddce8f4667dcde9d786`  
		Last Modified: Mon, 31 Mar 2025 19:28:45 GMT  
		Size: 14.4 KB (14360 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-alpine3.21`

```console
$ docker pull nats@sha256:222b8a7f2b9cbef1a51d412a5782ee75eac04062413d61c960b051e29c214115
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2-alpine3.21` - linux; amd64

```console
$ docker pull nats@sha256:d2bfc2b0b53f2a35c4b1c6fb432695b13dd232bdb551ea62c9fc00148520401f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10386128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6a871a4d4c93dc7e032ef72a3a722439e2ce32e96063585474891c6b654043f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
ENV NATS_SERVER=2.11.1-binary
# Mon, 31 Mar 2025 17:39:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='2499105f9e64bef55f168f634d34a586b710f6ac041639d8a18364f2b4f4c410' ;; 		armhf) natsArch='arm6'; sha256='31bc11906458e30c8028cdd0301de98713074db73f5e352f58ce4ecd6b1cc641' ;; 		armv7) natsArch='arm7'; sha256='432f4c47cf5adca05da67f1feaf969f6cea50ed9c3bb743a8bb76b8c5c583c8e' ;; 		x86_64) natsArch='amd64'; sha256='827497f99acd54eb0e4e8bfa3b0eb31dd51c6c259110de11a45a7fdacae6c5b3' ;; 		x86) natsArch='386'; sha256='651065e2170ee0f7e244425c0d0ba30a38776a7aef75e2d5cba0b8b11a950c54' ;; 		s390x) natsArch='s390x'; sha256='23e6ce6b70f9b973106d325eebb8bdd613040bedd4da980ff0aea2d2a7dc122e' ;; 		ppc64le) natsArch='ppc64le'; sha256='5341f41ef6298b05b72dd77c1ec055aeacb1b57dfd600ec888317347b3b4cbf8' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0643a146757fce88425f18db35388da5f1441b9e655395106fc3b6de8f7779a`  
		Last Modified: Mon, 31 Mar 2025 18:43:34 GMT  
		Size: 6.7 MB (6742912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f810863f848d47b0ec90164d81013c3f49b7d5d94bf9c42a73558dc7c46cfce`  
		Last Modified: Mon, 31 Mar 2025 18:43:33 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3295cd3199e071474b886bbbcf41ef4c12302ddbe5f1bd9283c8e119abcefe39`  
		Last Modified: Mon, 31 Mar 2025 18:43:33 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:7a817ee3d7045d87d4f49299e408201d1118ee221fdda63c5b66733871a32dea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89e54e9039e9d3c99605b12728bbecef9c9479593bdf67a68e894df9ecba60c4`

```dockerfile
```

-	Layers:
	-	`sha256:d380a2bbbdfb0718224f60b142dc29624483f0d28fa0552fb8e915ab9c1d69d2`  
		Last Modified: Mon, 31 Mar 2025 18:43:33 GMT  
		Size: 14.4 KB (14360 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.21` - linux; arm variant v6

```console
$ docker pull nats@sha256:5b003eca587d5d1ded87d52f52a88b49c6091e2ae6ffcbcc9591ef31edfb1153
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9830711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd78fe0bc28317f1acadcd3ed9a09443a843f5cf68ef058de361ff0570543e01`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
ENV NATS_SERVER=2.11.1-binary
# Mon, 31 Mar 2025 17:39:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='2499105f9e64bef55f168f634d34a586b710f6ac041639d8a18364f2b4f4c410' ;; 		armhf) natsArch='arm6'; sha256='31bc11906458e30c8028cdd0301de98713074db73f5e352f58ce4ecd6b1cc641' ;; 		armv7) natsArch='arm7'; sha256='432f4c47cf5adca05da67f1feaf969f6cea50ed9c3bb743a8bb76b8c5c583c8e' ;; 		x86_64) natsArch='amd64'; sha256='827497f99acd54eb0e4e8bfa3b0eb31dd51c6c259110de11a45a7fdacae6c5b3' ;; 		x86) natsArch='386'; sha256='651065e2170ee0f7e244425c0d0ba30a38776a7aef75e2d5cba0b8b11a950c54' ;; 		s390x) natsArch='s390x'; sha256='23e6ce6b70f9b973106d325eebb8bdd613040bedd4da980ff0aea2d2a7dc122e' ;; 		ppc64le) natsArch='ppc64le'; sha256='5341f41ef6298b05b72dd77c1ec055aeacb1b57dfd600ec888317347b3b4cbf8' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c92f9bdc82b0d8955653988d31a42d2d808133d9b313a6f16c7c1fc6187ce7c3`  
		Last Modified: Mon, 31 Mar 2025 18:50:14 GMT  
		Size: 6.5 MB (6465008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f8f3e30080f28fb154a8574bfa9e68094196baa500cc70232b4b6a993d7d96`  
		Last Modified: Mon, 31 Mar 2025 18:50:13 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b07ed84ffecb4fe35014c6ec28f044236b811f87738a6e32d50061b6cdcf8913`  
		Last Modified: Mon, 31 Mar 2025 18:50:13 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:25ca21f30fda2b87f68ede801458791fdf7fb7571b1dfc4c5b92a80f7287b667
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fa2e55e1097547a0c5dc17d479d5b338734fce9c9e83240bf6a9eb19569188a`

```dockerfile
```

-	Layers:
	-	`sha256:f659982640e897f8f52e71b1b320e9ea56d5354063a38cf666928fe3ccf97400`  
		Last Modified: Mon, 31 Mar 2025 18:50:13 GMT  
		Size: 14.5 KB (14468 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.21` - linux; arm variant v7

```console
$ docker pull nats@sha256:f6f902d9d220b13f8c52befb0e4f2520a530e999e9d0d7e3b4a7c96d1d6a2d4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9552225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f49a7e1e59161babacc6a62e07238abd7b349a8efc80a4bfd1523785ae8ece72`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
ENV NATS_SERVER=2.11.1-binary
# Mon, 31 Mar 2025 17:39:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='2499105f9e64bef55f168f634d34a586b710f6ac041639d8a18364f2b4f4c410' ;; 		armhf) natsArch='arm6'; sha256='31bc11906458e30c8028cdd0301de98713074db73f5e352f58ce4ecd6b1cc641' ;; 		armv7) natsArch='arm7'; sha256='432f4c47cf5adca05da67f1feaf969f6cea50ed9c3bb743a8bb76b8c5c583c8e' ;; 		x86_64) natsArch='amd64'; sha256='827497f99acd54eb0e4e8bfa3b0eb31dd51c6c259110de11a45a7fdacae6c5b3' ;; 		x86) natsArch='386'; sha256='651065e2170ee0f7e244425c0d0ba30a38776a7aef75e2d5cba0b8b11a950c54' ;; 		s390x) natsArch='s390x'; sha256='23e6ce6b70f9b973106d325eebb8bdd613040bedd4da980ff0aea2d2a7dc122e' ;; 		ppc64le) natsArch='ppc64le'; sha256='5341f41ef6298b05b72dd77c1ec055aeacb1b57dfd600ec888317347b3b4cbf8' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4be7f6d278a4174ef17dcd8c89848f067134976f430004cbed069643b89e46e8`  
		Last Modified: Mon, 31 Mar 2025 20:17:05 GMT  
		Size: 6.5 MB (6453133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825c724725f466486a81cdde1ec6a92840eb03f19fc7c9f6c2361d13f3398293`  
		Last Modified: Mon, 31 Mar 2025 20:17:04 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe87685444a72475e87e5ffbb1baff8c65017859e8e53c72573fc546273e8ef6`  
		Last Modified: Mon, 31 Mar 2025 20:17:04 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:860dd6d0c495dc91deb8a4c27e98247c01e7cc5ba0a4a80d0e33430aaa5695db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41756094504db64ff2b19360c941882401645db6e11cb7b116c9cc5d965c1002`

```dockerfile
```

-	Layers:
	-	`sha256:a83dd1e9193bcbd50a20cfab9ac07e63cb0d3f71b71000fc9b9e4456a63ddc2c`  
		Last Modified: Mon, 31 Mar 2025 20:17:04 GMT  
		Size: 14.5 KB (14468 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:90874ce66332c5ed35925509121cc1231be38266af7f5efe7097f37a54610dc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10234990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e934c9514dbf2966156ca2a5b60a8c62eab86a1d0e9316d96e587bc52837aff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
ENV NATS_SERVER=2.11.1-binary
# Mon, 31 Mar 2025 17:39:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='2499105f9e64bef55f168f634d34a586b710f6ac041639d8a18364f2b4f4c410' ;; 		armhf) natsArch='arm6'; sha256='31bc11906458e30c8028cdd0301de98713074db73f5e352f58ce4ecd6b1cc641' ;; 		armv7) natsArch='arm7'; sha256='432f4c47cf5adca05da67f1feaf969f6cea50ed9c3bb743a8bb76b8c5c583c8e' ;; 		x86_64) natsArch='amd64'; sha256='827497f99acd54eb0e4e8bfa3b0eb31dd51c6c259110de11a45a7fdacae6c5b3' ;; 		x86) natsArch='386'; sha256='651065e2170ee0f7e244425c0d0ba30a38776a7aef75e2d5cba0b8b11a950c54' ;; 		s390x) natsArch='s390x'; sha256='23e6ce6b70f9b973106d325eebb8bdd613040bedd4da980ff0aea2d2a7dc122e' ;; 		ppc64le) natsArch='ppc64le'; sha256='5341f41ef6298b05b72dd77c1ec055aeacb1b57dfd600ec888317347b3b4cbf8' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60797fdb0b4d910be869065ae81ab51200fbe5544785eb4efa8fc7cb9eb3033e`  
		Last Modified: Mon, 31 Mar 2025 20:11:13 GMT  
		Size: 6.2 MB (6240991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dda5bbcac3d56d1f2414331f89b9333ef3393083b91ce07a2face8802428335`  
		Last Modified: Mon, 31 Mar 2025 20:11:12 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c42e24e15c065a92a28be68d337a0e3f21fc9b4bee9e5e931179ab16a647031`  
		Last Modified: Mon, 31 Mar 2025 20:11:12 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:061fa681d240f27b08e83d14d855bff8191035c3944adf647afab28af9d67b5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a76bc64a67b68410441588e0e8ebc82c70ec9260099bfb6d4d5154152785d62`

```dockerfile
```

-	Layers:
	-	`sha256:5b3a7763692c9fffeebb31f53b8a14d7192250292c1661653d8912d27e67bd34`  
		Last Modified: Mon, 31 Mar 2025 20:11:12 GMT  
		Size: 14.5 KB (14512 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.21` - linux; ppc64le

```console
$ docker pull nats@sha256:f09b96d5bfacda0649814f91facba68b0ecca96de4ebdea7e17dfde79f1ada96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9796685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10c6bb2aed5161b870f53898cce57635999f3e6368d89209be712832cb7caae3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
ENV NATS_SERVER=2.11.1-binary
# Mon, 31 Mar 2025 17:39:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='2499105f9e64bef55f168f634d34a586b710f6ac041639d8a18364f2b4f4c410' ;; 		armhf) natsArch='arm6'; sha256='31bc11906458e30c8028cdd0301de98713074db73f5e352f58ce4ecd6b1cc641' ;; 		armv7) natsArch='arm7'; sha256='432f4c47cf5adca05da67f1feaf969f6cea50ed9c3bb743a8bb76b8c5c583c8e' ;; 		x86_64) natsArch='amd64'; sha256='827497f99acd54eb0e4e8bfa3b0eb31dd51c6c259110de11a45a7fdacae6c5b3' ;; 		x86) natsArch='386'; sha256='651065e2170ee0f7e244425c0d0ba30a38776a7aef75e2d5cba0b8b11a950c54' ;; 		s390x) natsArch='s390x'; sha256='23e6ce6b70f9b973106d325eebb8bdd613040bedd4da980ff0aea2d2a7dc122e' ;; 		ppc64le) natsArch='ppc64le'; sha256='5341f41ef6298b05b72dd77c1ec055aeacb1b57dfd600ec888317347b3b4cbf8' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:299c0ee564e4568e71d43a566874e9d853458071d554386ad5728913e55f5d42`  
		Last Modified: Mon, 31 Mar 2025 19:45:06 GMT  
		Size: 6.2 MB (6221370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1af98871a1453d715b201d0cb6c30c2e8240dd12ee7af67f4334bfb80877f3bb`  
		Last Modified: Mon, 31 Mar 2025 19:45:05 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:103d308786c4f17ef7f21746eadc69443e28518b33fd5534040a513bbb5acc64`  
		Last Modified: Mon, 31 Mar 2025 19:45:05 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:261ca6909da20cd9b36804c44211d5a257a4f0a8746e425a8d63cebe1ff274eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bf43f070134532bf9419111138ee6504a3b9010b90d59e6380375b5b9a4abcf`

```dockerfile
```

-	Layers:
	-	`sha256:09877c6dec89674d2ec4aefc8edd75ff573a4834ca2851e1a4be89994ffcd528`  
		Last Modified: Mon, 31 Mar 2025 19:45:05 GMT  
		Size: 14.4 KB (14427 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.21` - linux; s390x

```console
$ docker pull nats@sha256:c14e89986785ed37ac2931d4b307ea84375f49180341e48c9024fe40f226decc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10053962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:893690471f61ea43e10126b7ceb4fd7a07fd98eb86fff95edc6cd8cf10d1e4ef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
ENV NATS_SERVER=2.11.1-binary
# Mon, 31 Mar 2025 17:39:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='2499105f9e64bef55f168f634d34a586b710f6ac041639d8a18364f2b4f4c410' ;; 		armhf) natsArch='arm6'; sha256='31bc11906458e30c8028cdd0301de98713074db73f5e352f58ce4ecd6b1cc641' ;; 		armv7) natsArch='arm7'; sha256='432f4c47cf5adca05da67f1feaf969f6cea50ed9c3bb743a8bb76b8c5c583c8e' ;; 		x86_64) natsArch='amd64'; sha256='827497f99acd54eb0e4e8bfa3b0eb31dd51c6c259110de11a45a7fdacae6c5b3' ;; 		x86) natsArch='386'; sha256='651065e2170ee0f7e244425c0d0ba30a38776a7aef75e2d5cba0b8b11a950c54' ;; 		s390x) natsArch='s390x'; sha256='23e6ce6b70f9b973106d325eebb8bdd613040bedd4da980ff0aea2d2a7dc122e' ;; 		ppc64le) natsArch='ppc64le'; sha256='5341f41ef6298b05b72dd77c1ec055aeacb1b57dfd600ec888317347b3b4cbf8' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67f000d40cf6813dabcb134d2a9b15f3b7eb5ba7dba583ad1df023b35efd9ca`  
		Last Modified: Mon, 31 Mar 2025 19:28:46 GMT  
		Size: 6.6 MB (6585424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4501a9ec92d7d9a89fd0e10cd2ba4c8fb93658a4d46301543d45d1f96b07ce32`  
		Last Modified: Mon, 31 Mar 2025 19:28:45 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06c2b65e72a2a266d2d783396559cd0ee8346a11e25f65ca2b21cc82de4174b6`  
		Last Modified: Mon, 31 Mar 2025 19:28:45 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:82ec15847478c49a8a561d7f21d2239bbea2614e277659456213e6bdd0f5dd49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:443d1aa445d5406aada9c0970885e837d983ea976af12760bad0de2704481f16`

```dockerfile
```

-	Layers:
	-	`sha256:688e4b2d5f0fdef107c3405864e3c9cc14ae13fd320ceddce8f4667dcde9d786`  
		Last Modified: Mon, 31 Mar 2025 19:28:45 GMT  
		Size: 14.4 KB (14360 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-linux`

```console
$ docker pull nats@sha256:c81104c29f774ab6ac6178391029a857ca1b201750c9ebefad70bee0b9162cf6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2-linux` - linux; amd64

```console
$ docker pull nats@sha256:0b313c16824b8d98736c06153fa01af3c8d62eebc6298e9062fd2e00c0a3e865
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6282666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5a2333da61b6c9f0de1de8235aca52ee071283b0c8c6487d3ea15b4a0f9f8e2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:54120e60f5a574cbbfd83de2711330ae98499a27ff592bdb694994b87749dd23`  
		Last Modified: Mon, 31 Mar 2025 17:41:30 GMT  
		Size: 6.3 MB (6282155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71d71c31c70e45e814d8db85102321f1459be653c595cd91fafb76306cdf405e`  
		Last Modified: Mon, 31 Mar 2025 19:07:36 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:b8d62bc797363d5eab76aea96ec144d02b901da4dba8eb8bf31cc4e51e3a09d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbd51cd5b25ea5c4355cd2cde0e286d4f6da98802af9ed8b477001ff7ece4679`

```dockerfile
```

-	Layers:
	-	`sha256:19abc39a4cbb247bfa12363ce59bbce1e3bf861fddb9055c3a17e2d39d54d204`  
		Last Modified: Mon, 31 Mar 2025 19:07:36 GMT  
		Size: 10.5 KB (10523 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:af5758489c2981e0a1028dc47f82f0dd2d26e2fac7ac1e478a2a15a12029f6d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6002169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c17f13cf88d7cb6d029eafd34cd847cbacebb2131dc5b7ecfbed791e2958e6a4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:098bda892a4e7ddd77ca838f72ef9757e9b3cfae3c7bc97076a8dd0b6fd92597`  
		Last Modified: Mon, 31 Mar 2025 17:41:30 GMT  
		Size: 6.0 MB (6001660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff1d2651842734b21329c25e1004a4da19102e57001381e60bb4fd58723fe19`  
		Last Modified: Mon, 31 Mar 2025 19:07:08 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:736b8ee8472809de9731d9c426d2113e533e5ac68c9fbf4cd6bb44eb636b3d79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ffa52afcf9f827961f6f692daeb94f398721ac7559f559d56147558f6742150`

```dockerfile
```

-	Layers:
	-	`sha256:cc5887e8b88d73925b5364f9143ca37566f003a1560dffe173f7be8f10d66806`  
		Last Modified: Mon, 31 Mar 2025 19:07:08 GMT  
		Size: 10.7 KB (10650 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:f1752b6d8b3a5506fab1fdf93ce66a6bd6e934d33a3c230231458f254ff505a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5992492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68d3d700cbec0d68868397c08f331e9cee8a3e484035ab651de2414c1bc1039b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7ae07ef7aadc186e26516a3b1a5bacd27b42c41b8d63efc540622587ef29be07`  
		Last Modified: Mon, 31 Mar 2025 17:41:36 GMT  
		Size: 6.0 MB (5991983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d132fb7bc19f6f368e535b5a46903e88d661e5c0f5e33c79b7d66b962039598`  
		Last Modified: Mon, 31 Mar 2025 20:44:23 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:ff00ada993e928a0dbcd0e627e845b5f9c4d11042f0e089912b8ef2969c89876
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab26b373d46f30d56fc9b9ecf02d3c518eb5ab041a8fbb69e562b49b1a864d9d`

```dockerfile
```

-	Layers:
	-	`sha256:d552b4d64ce37965149a8aaeed3a0eebd251066efc77cb63ad2307f9d0bbdef7`  
		Last Modified: Mon, 31 Mar 2025 20:44:23 GMT  
		Size: 10.6 KB (10649 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a360fbbfeb6f19012e875675cf70ea15e5ea3d9e003d5ccf1a61adeed8d515c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5776951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aad8d86003a865c09c995830bd52c9154c44e7976be35a0790b217a28445c6c2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:813138f2f23c3f67c00cc3f899e890b4b46ad187b3c70730ab91bd63ff37fa6d`  
		Last Modified: Mon, 31 Mar 2025 17:41:30 GMT  
		Size: 5.8 MB (5776442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d132fb7bc19f6f368e535b5a46903e88d661e5c0f5e33c79b7d66b962039598`  
		Last Modified: Mon, 31 Mar 2025 20:44:23 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:13fe1989809a4185209660bba2e8a407b921e80a959889e94c8d6b18e6eadc66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cebd7eb7627ea55d24e6c1b36e5124796e00e1a2243414d5b3f65ff44089ec66`

```dockerfile
```

-	Layers:
	-	`sha256:a33f391d8364f479953478aa1b1ce3f8e6e05c31407e5d9ead5d4d5db6da559f`  
		Last Modified: Mon, 31 Mar 2025 20:44:29 GMT  
		Size: 10.7 KB (10708 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:74e2df57ac704452ee531238216b3accd76025199ee310563732dd2c680227a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5757216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abd71cf45edbcaea354422b03a686d602fac79be9357fdbc6b5c05d8ab8309e5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:452917a8c6e0add88a19efed21ff3bf850d722622f476c3b9d4426f3dbaaffb7`  
		Last Modified: Mon, 31 Mar 2025 17:41:27 GMT  
		Size: 5.8 MB (5756706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc09a85b63b7a6867f196c8c27905ad711a7457fa91d3df80022bc3d24111b3`  
		Last Modified: Mon, 31 Mar 2025 20:07:44 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:9460476db24c3ccd45c6374ab5e0dfa8af2b95e6ed003b294fca69a3f6d49e72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8048c19445dcae5f87494cedbc4822265fb6848963d3958920bc8a77dc19881`

```dockerfile
```

-	Layers:
	-	`sha256:2e79f43f61fe3cbbfb9fa2ab55acbd3a3254d4378c81f4bef4392b1b18e91f10`  
		Last Modified: Mon, 31 Mar 2025 20:07:44 GMT  
		Size: 10.6 KB (10613 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; s390x

```console
$ docker pull nats@sha256:6b9323c60c161cbd82daa5b02f46e55051f8540e7c9770dc1c2ed619086c6f53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6122555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb48b95165c0163d0de0d793f09fa9aaa8dbc79c4b50241ee9e33ac819b1a501`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:cdb5d3b73d4e5760c377e2d1a31f668fd95251ac45157f6a4c4d98139b337e23`  
		Last Modified: Mon, 31 Mar 2025 17:41:31 GMT  
		Size: 6.1 MB (6122046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16e9431fd0e418054b688573b0ef6c205ce09bcb9015c474b01a32d6800912d0`  
		Last Modified: Mon, 31 Mar 2025 20:07:36 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:2dfb1482f9d33c4a0f01a77e40b206f5b997b290b5e3899ee0c2678dd35731a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff58880fe981b8b31c473e8e992460d1ef7a218db9dd4ffc3a951750055bfd3`

```dockerfile
```

-	Layers:
	-	`sha256:9bb52fda18a732bf8f1ead6cd17dd200cfcae43fd84710a4ddb71372c0815f2b`  
		Last Modified: Mon, 31 Mar 2025 20:07:36 GMT  
		Size: 10.5 KB (10523 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-nanoserver`

```console
$ docker pull nats@sha256:ab7919f36b0bf7f8b85e92aadeb04b95a0f3a5f1d2b33203d2ed60c8104ef5ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `nats:2-nanoserver` - windows version 10.0.17763.7009; amd64

```console
$ docker pull nats@sha256:7523855e64c122a386122c97e7e122f78929c93ef1aaeabcfb818f96108eb526
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.4 MB (113369799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59c769ae1c19e869c3ab50a8bcc53b7a416139faa1f967bef29391891ff94a43`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 05 Mar 2025 21:54:26 GMT
RUN Apply image 10.0.17763.7009
# Mon, 31 Mar 2025 19:16:51 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Mon, 31 Mar 2025 19:16:54 GMT
RUN cmd /S /C #(nop) COPY file:cbd316e46d1e3baa5a0ffb6e227be5b521aa07a7cbe3a0513c0076ac28429bf3 in C:\nats-server.exe 
# Mon, 31 Mar 2025 19:16:55 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Mon, 31 Mar 2025 19:16:55 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Mon, 31 Mar 2025 19:16:56 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 31 Mar 2025 19:16:56 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:543388a101bf4d470af7e8817eff3f6f3b98f13d106939ab3f507a28f2825d0a`  
		Last Modified: Tue, 11 Mar 2025 22:40:48 GMT  
		Size: 106.9 MB (106907688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5764592bce5a260f59c0fc8af513aa702c03e73d61b9d9769cfb463cb5d345a4`  
		Last Modified: Mon, 31 Mar 2025 19:17:00 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c220ae7f5568ad8b19e77200fe2ab8b43bd7e66c8215b73f18cab048bf4c949b`  
		Last Modified: Mon, 31 Mar 2025 19:16:59 GMT  
		Size: 6.5 MB (6456094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24b9abd521fc3bf26173541357dca364e2aaa425fa95150aa12063ad86adbd0f`  
		Last Modified: Mon, 31 Mar 2025 19:16:59 GMT  
		Size: 1.7 KB (1684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47263123c2dca13a6ccd5e6c3f836df870102b1186585b3533a50841169f2d5d`  
		Last Modified: Mon, 31 Mar 2025 19:16:59 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb4c62df8bd6d5f27aca099be80d7290759022e9ed845409d9608b11f0e3db16`  
		Last Modified: Mon, 31 Mar 2025 19:16:58 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faf623903ff066d1e92e2c9250d8f7cd5a3230c1ea39d9cbe269fd63e735f4be`  
		Last Modified: Mon, 31 Mar 2025 19:16:59 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver-1809`

```console
$ docker pull nats@sha256:ab7919f36b0bf7f8b85e92aadeb04b95a0f3a5f1d2b33203d2ed60c8104ef5ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `nats:2-nanoserver-1809` - windows version 10.0.17763.7009; amd64

```console
$ docker pull nats@sha256:7523855e64c122a386122c97e7e122f78929c93ef1aaeabcfb818f96108eb526
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.4 MB (113369799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59c769ae1c19e869c3ab50a8bcc53b7a416139faa1f967bef29391891ff94a43`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 05 Mar 2025 21:54:26 GMT
RUN Apply image 10.0.17763.7009
# Mon, 31 Mar 2025 19:16:51 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Mon, 31 Mar 2025 19:16:54 GMT
RUN cmd /S /C #(nop) COPY file:cbd316e46d1e3baa5a0ffb6e227be5b521aa07a7cbe3a0513c0076ac28429bf3 in C:\nats-server.exe 
# Mon, 31 Mar 2025 19:16:55 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Mon, 31 Mar 2025 19:16:55 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Mon, 31 Mar 2025 19:16:56 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 31 Mar 2025 19:16:56 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:543388a101bf4d470af7e8817eff3f6f3b98f13d106939ab3f507a28f2825d0a`  
		Last Modified: Tue, 11 Mar 2025 22:40:48 GMT  
		Size: 106.9 MB (106907688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5764592bce5a260f59c0fc8af513aa702c03e73d61b9d9769cfb463cb5d345a4`  
		Last Modified: Mon, 31 Mar 2025 19:17:00 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c220ae7f5568ad8b19e77200fe2ab8b43bd7e66c8215b73f18cab048bf4c949b`  
		Last Modified: Mon, 31 Mar 2025 19:16:59 GMT  
		Size: 6.5 MB (6456094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24b9abd521fc3bf26173541357dca364e2aaa425fa95150aa12063ad86adbd0f`  
		Last Modified: Mon, 31 Mar 2025 19:16:59 GMT  
		Size: 1.7 KB (1684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47263123c2dca13a6ccd5e6c3f836df870102b1186585b3533a50841169f2d5d`  
		Last Modified: Mon, 31 Mar 2025 19:16:59 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb4c62df8bd6d5f27aca099be80d7290759022e9ed845409d9608b11f0e3db16`  
		Last Modified: Mon, 31 Mar 2025 19:16:58 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faf623903ff066d1e92e2c9250d8f7cd5a3230c1ea39d9cbe269fd63e735f4be`  
		Last Modified: Mon, 31 Mar 2025 19:16:59 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-scratch`

```console
$ docker pull nats@sha256:c81104c29f774ab6ac6178391029a857ca1b201750c9ebefad70bee0b9162cf6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2-scratch` - linux; amd64

```console
$ docker pull nats@sha256:0b313c16824b8d98736c06153fa01af3c8d62eebc6298e9062fd2e00c0a3e865
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6282666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5a2333da61b6c9f0de1de8235aca52ee071283b0c8c6487d3ea15b4a0f9f8e2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:54120e60f5a574cbbfd83de2711330ae98499a27ff592bdb694994b87749dd23`  
		Last Modified: Mon, 31 Mar 2025 17:41:30 GMT  
		Size: 6.3 MB (6282155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71d71c31c70e45e814d8db85102321f1459be653c595cd91fafb76306cdf405e`  
		Last Modified: Mon, 31 Mar 2025 19:07:36 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:b8d62bc797363d5eab76aea96ec144d02b901da4dba8eb8bf31cc4e51e3a09d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbd51cd5b25ea5c4355cd2cde0e286d4f6da98802af9ed8b477001ff7ece4679`

```dockerfile
```

-	Layers:
	-	`sha256:19abc39a4cbb247bfa12363ce59bbce1e3bf861fddb9055c3a17e2d39d54d204`  
		Last Modified: Mon, 31 Mar 2025 19:07:36 GMT  
		Size: 10.5 KB (10523 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:af5758489c2981e0a1028dc47f82f0dd2d26e2fac7ac1e478a2a15a12029f6d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6002169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c17f13cf88d7cb6d029eafd34cd847cbacebb2131dc5b7ecfbed791e2958e6a4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:098bda892a4e7ddd77ca838f72ef9757e9b3cfae3c7bc97076a8dd0b6fd92597`  
		Last Modified: Mon, 31 Mar 2025 17:41:30 GMT  
		Size: 6.0 MB (6001660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff1d2651842734b21329c25e1004a4da19102e57001381e60bb4fd58723fe19`  
		Last Modified: Mon, 31 Mar 2025 19:07:08 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:736b8ee8472809de9731d9c426d2113e533e5ac68c9fbf4cd6bb44eb636b3d79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ffa52afcf9f827961f6f692daeb94f398721ac7559f559d56147558f6742150`

```dockerfile
```

-	Layers:
	-	`sha256:cc5887e8b88d73925b5364f9143ca37566f003a1560dffe173f7be8f10d66806`  
		Last Modified: Mon, 31 Mar 2025 19:07:08 GMT  
		Size: 10.7 KB (10650 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:f1752b6d8b3a5506fab1fdf93ce66a6bd6e934d33a3c230231458f254ff505a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5992492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68d3d700cbec0d68868397c08f331e9cee8a3e484035ab651de2414c1bc1039b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7ae07ef7aadc186e26516a3b1a5bacd27b42c41b8d63efc540622587ef29be07`  
		Last Modified: Mon, 31 Mar 2025 17:41:36 GMT  
		Size: 6.0 MB (5991983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d132fb7bc19f6f368e535b5a46903e88d661e5c0f5e33c79b7d66b962039598`  
		Last Modified: Mon, 31 Mar 2025 20:44:23 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:ff00ada993e928a0dbcd0e627e845b5f9c4d11042f0e089912b8ef2969c89876
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab26b373d46f30d56fc9b9ecf02d3c518eb5ab041a8fbb69e562b49b1a864d9d`

```dockerfile
```

-	Layers:
	-	`sha256:d552b4d64ce37965149a8aaeed3a0eebd251066efc77cb63ad2307f9d0bbdef7`  
		Last Modified: Mon, 31 Mar 2025 20:44:23 GMT  
		Size: 10.6 KB (10649 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a360fbbfeb6f19012e875675cf70ea15e5ea3d9e003d5ccf1a61adeed8d515c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5776951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aad8d86003a865c09c995830bd52c9154c44e7976be35a0790b217a28445c6c2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:813138f2f23c3f67c00cc3f899e890b4b46ad187b3c70730ab91bd63ff37fa6d`  
		Last Modified: Mon, 31 Mar 2025 17:41:30 GMT  
		Size: 5.8 MB (5776442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d132fb7bc19f6f368e535b5a46903e88d661e5c0f5e33c79b7d66b962039598`  
		Last Modified: Mon, 31 Mar 2025 20:44:23 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:13fe1989809a4185209660bba2e8a407b921e80a959889e94c8d6b18e6eadc66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cebd7eb7627ea55d24e6c1b36e5124796e00e1a2243414d5b3f65ff44089ec66`

```dockerfile
```

-	Layers:
	-	`sha256:a33f391d8364f479953478aa1b1ce3f8e6e05c31407e5d9ead5d4d5db6da559f`  
		Last Modified: Mon, 31 Mar 2025 20:44:29 GMT  
		Size: 10.7 KB (10708 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:74e2df57ac704452ee531238216b3accd76025199ee310563732dd2c680227a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5757216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abd71cf45edbcaea354422b03a686d602fac79be9357fdbc6b5c05d8ab8309e5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:452917a8c6e0add88a19efed21ff3bf850d722622f476c3b9d4426f3dbaaffb7`  
		Last Modified: Mon, 31 Mar 2025 17:41:27 GMT  
		Size: 5.8 MB (5756706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc09a85b63b7a6867f196c8c27905ad711a7457fa91d3df80022bc3d24111b3`  
		Last Modified: Mon, 31 Mar 2025 20:07:44 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:9460476db24c3ccd45c6374ab5e0dfa8af2b95e6ed003b294fca69a3f6d49e72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8048c19445dcae5f87494cedbc4822265fb6848963d3958920bc8a77dc19881`

```dockerfile
```

-	Layers:
	-	`sha256:2e79f43f61fe3cbbfb9fa2ab55acbd3a3254d4378c81f4bef4392b1b18e91f10`  
		Last Modified: Mon, 31 Mar 2025 20:07:44 GMT  
		Size: 10.6 KB (10613 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; s390x

```console
$ docker pull nats@sha256:6b9323c60c161cbd82daa5b02f46e55051f8540e7c9770dc1c2ed619086c6f53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6122555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb48b95165c0163d0de0d793f09fa9aaa8dbc79c4b50241ee9e33ac819b1a501`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:cdb5d3b73d4e5760c377e2d1a31f668fd95251ac45157f6a4c4d98139b337e23`  
		Last Modified: Mon, 31 Mar 2025 17:41:31 GMT  
		Size: 6.1 MB (6122046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16e9431fd0e418054b688573b0ef6c205ce09bcb9015c474b01a32d6800912d0`  
		Last Modified: Mon, 31 Mar 2025 20:07:36 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:2dfb1482f9d33c4a0f01a77e40b206f5b997b290b5e3899ee0c2678dd35731a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff58880fe981b8b31c473e8e992460d1ef7a218db9dd4ffc3a951750055bfd3`

```dockerfile
```

-	Layers:
	-	`sha256:9bb52fda18a732bf8f1ead6cd17dd200cfcae43fd84710a4ddb71372c0815f2b`  
		Last Modified: Mon, 31 Mar 2025 20:07:36 GMT  
		Size: 10.5 KB (10523 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-windowsservercore`

```console
$ docker pull nats@sha256:9d03bcf6cbd1a06b72b01b12931276f9f11d428800308790ac7d2c5e7f013153
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `nats:2-windowsservercore` - windows version 10.0.17763.7009; amd64

```console
$ docker pull nats@sha256:358cd0aed79a204ff4c8b5c055a03c487c5358d7455e0ffa579125eceef0d34e
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2158788658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ee73222ac79929936f4b58dc26a22b9521b1d61e7a78f7c5ed88a75f23f1374`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 05 Mar 2025 22:09:20 GMT
RUN Install update 10.0.17763.7009
# Mon, 31 Mar 2025 18:52:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 31 Mar 2025 18:52:57 GMT
ENV NATS_DOCKERIZED=1
# Mon, 31 Mar 2025 18:52:58 GMT
ENV NATS_SERVER=2.11.1-binary
# Mon, 31 Mar 2025 18:52:59 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.1-binary/nats-server-v2.11.1-binary-windows-amd64.zip
# Mon, 31 Mar 2025 18:52:59 GMT
ENV NATS_SERVER_SHASUM=2ab6b2c964fd5fe3b10a471cba309033f0756182f69228a65d1764197facf59c
# Mon, 31 Mar 2025 18:53:46 GMT
RUN Set-PSDebug -Trace 2
# Mon, 31 Mar 2025 18:54:06 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Mon, 31 Mar 2025 18:54:06 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Mon, 31 Mar 2025 18:54:07 GMT
EXPOSE 4222 6222 8222
# Mon, 31 Mar 2025 18:54:08 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 31 Mar 2025 18:54:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77bec5e4bac3c7f6dc5d56da5ffc11e72881485b3a55330c17c915ad653f955`  
		Last Modified: Tue, 11 Mar 2025 17:48:06 GMT  
		Size: 431.4 MB (431366277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35a6c48e83b6ecc670f12e09411b9f19d7fb0a878e1f86a6812563467340ff8`  
		Last Modified: Mon, 31 Mar 2025 18:54:13 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c158e67ae1fa853b1e146c6dd4e2b8f7e13aab94075904e788f4dfa3b8943322`  
		Last Modified: Mon, 31 Mar 2025 18:54:12 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6610f67e82d540d4cf11d12f87f1a68f8b42e4371905c52df1cade737e4f44c`  
		Last Modified: Mon, 31 Mar 2025 18:54:11 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0929886be3ca1628c185214c762369ea53c4afb47d0603d3d69fb4b471d01bf7`  
		Last Modified: Mon, 31 Mar 2025 18:54:12 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a89f7e18c6f6e8406fbe811630282ddd985e8899085b73506a0f39ac3c8fcf33`  
		Last Modified: Mon, 31 Mar 2025 18:54:11 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a904ed39f5ad31d12b93284fed611d377be64b1d3871e896c2e1c83415ff28`  
		Last Modified: Mon, 31 Mar 2025 18:54:11 GMT  
		Size: 333.8 KB (333807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5239d01ea32c2be9edfc2b25b142685efcbaedbadb1778166b52c0858df66464`  
		Last Modified: Mon, 31 Mar 2025 18:54:11 GMT  
		Size: 6.8 MB (6807873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56c6af05e936d2967cd915bd57f5faacef8b514317cd4de730f837f728d14487`  
		Last Modified: Mon, 31 Mar 2025 18:54:10 GMT  
		Size: 1.9 KB (1931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe56937824b786b5d064fe15be3435e14f26a022d00662003396c61194954e0`  
		Last Modified: Mon, 31 Mar 2025 18:54:10 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4aaffd9d1722fd09e9a67ad18073b6716178658c1f5517404d7b4180df3142f`  
		Last Modified: Mon, 31 Mar 2025 18:54:10 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdcbf0f98ff7504665d65ee0034ca94a89e45d2ecc47f808f87787d51427d265`  
		Last Modified: Mon, 31 Mar 2025 18:54:10 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-1809`

```console
$ docker pull nats@sha256:9d03bcf6cbd1a06b72b01b12931276f9f11d428800308790ac7d2c5e7f013153
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `nats:2-windowsservercore-1809` - windows version 10.0.17763.7009; amd64

```console
$ docker pull nats@sha256:358cd0aed79a204ff4c8b5c055a03c487c5358d7455e0ffa579125eceef0d34e
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2158788658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ee73222ac79929936f4b58dc26a22b9521b1d61e7a78f7c5ed88a75f23f1374`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 05 Mar 2025 22:09:20 GMT
RUN Install update 10.0.17763.7009
# Mon, 31 Mar 2025 18:52:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 31 Mar 2025 18:52:57 GMT
ENV NATS_DOCKERIZED=1
# Mon, 31 Mar 2025 18:52:58 GMT
ENV NATS_SERVER=2.11.1-binary
# Mon, 31 Mar 2025 18:52:59 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.1-binary/nats-server-v2.11.1-binary-windows-amd64.zip
# Mon, 31 Mar 2025 18:52:59 GMT
ENV NATS_SERVER_SHASUM=2ab6b2c964fd5fe3b10a471cba309033f0756182f69228a65d1764197facf59c
# Mon, 31 Mar 2025 18:53:46 GMT
RUN Set-PSDebug -Trace 2
# Mon, 31 Mar 2025 18:54:06 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Mon, 31 Mar 2025 18:54:06 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Mon, 31 Mar 2025 18:54:07 GMT
EXPOSE 4222 6222 8222
# Mon, 31 Mar 2025 18:54:08 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 31 Mar 2025 18:54:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77bec5e4bac3c7f6dc5d56da5ffc11e72881485b3a55330c17c915ad653f955`  
		Last Modified: Tue, 11 Mar 2025 17:48:06 GMT  
		Size: 431.4 MB (431366277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35a6c48e83b6ecc670f12e09411b9f19d7fb0a878e1f86a6812563467340ff8`  
		Last Modified: Mon, 31 Mar 2025 18:54:13 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c158e67ae1fa853b1e146c6dd4e2b8f7e13aab94075904e788f4dfa3b8943322`  
		Last Modified: Mon, 31 Mar 2025 18:54:12 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6610f67e82d540d4cf11d12f87f1a68f8b42e4371905c52df1cade737e4f44c`  
		Last Modified: Mon, 31 Mar 2025 18:54:11 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0929886be3ca1628c185214c762369ea53c4afb47d0603d3d69fb4b471d01bf7`  
		Last Modified: Mon, 31 Mar 2025 18:54:12 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a89f7e18c6f6e8406fbe811630282ddd985e8899085b73506a0f39ac3c8fcf33`  
		Last Modified: Mon, 31 Mar 2025 18:54:11 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a904ed39f5ad31d12b93284fed611d377be64b1d3871e896c2e1c83415ff28`  
		Last Modified: Mon, 31 Mar 2025 18:54:11 GMT  
		Size: 333.8 KB (333807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5239d01ea32c2be9edfc2b25b142685efcbaedbadb1778166b52c0858df66464`  
		Last Modified: Mon, 31 Mar 2025 18:54:11 GMT  
		Size: 6.8 MB (6807873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56c6af05e936d2967cd915bd57f5faacef8b514317cd4de730f837f728d14487`  
		Last Modified: Mon, 31 Mar 2025 18:54:10 GMT  
		Size: 1.9 KB (1931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe56937824b786b5d064fe15be3435e14f26a022d00662003396c61194954e0`  
		Last Modified: Mon, 31 Mar 2025 18:54:10 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4aaffd9d1722fd09e9a67ad18073b6716178658c1f5517404d7b4180df3142f`  
		Last Modified: Mon, 31 Mar 2025 18:54:10 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdcbf0f98ff7504665d65ee0034ca94a89e45d2ecc47f808f87787d51427d265`  
		Last Modified: Mon, 31 Mar 2025 18:54:10 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10`

```console
$ docker pull nats@sha256:383481d9952319e082c015634febccc61c74ffeb3a924bce8fdcf77f26f1b8f2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 13
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown
	-	windows version 10.0.17763.7009; amd64

### `nats:2.10` - linux; amd64

```console
$ docker pull nats@sha256:3d3b2708e7710851a833987f3e530347d7659bba76aeace72d6f464933d57550
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6168972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65961e39279d1ae6a339ac8974109034f1ebe3d7d5a5099eaf38be54ac268706`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5b579bbe96b7482253ae3b409416bbdfaf291d6d7244c3f5fc020b18b653565a`  
		Last Modified: Mon, 31 Mar 2025 17:41:17 GMT  
		Size: 6.2 MB (6168462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:046faf28dbdb891d978b08adfc464a48ba8a6e73a4758a820994b4ce63d0b42f`  
		Last Modified: Mon, 31 Mar 2025 19:07:44 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:afe941a29e96dad9907c501b5b6787daae9cfa9146ddd8f8fd2f161684452249
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5523d84636ff676596da2cadbb6c81987810c613a7d2a05d8e427672b95674f`

```dockerfile
```

-	Layers:
	-	`sha256:acf00ab6fca0df765d7927dce65081e34a17483230da3b9fe95a04c3db26a10b`  
		Last Modified: Mon, 31 Mar 2025 19:07:44 GMT  
		Size: 8.8 KB (8771 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - linux; arm variant v6

```console
$ docker pull nats@sha256:3e5bffb909e76fd626bf774d58bb506d2a1101cf5d326c48fd2f9fd2b6b22df9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5892862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd79b95b8dc7a7de4ef505d7da015ccb8695dcaf721e571a5b167f50f7f8c90f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:705eaca27bc0bc30ef31a1c6ffa4e80af4a0314dcd595126dea159490cf9bc6c`  
		Last Modified: Mon, 31 Mar 2025 17:41:16 GMT  
		Size: 5.9 MB (5892354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ce9d4ac346e66940eb00e34686597227c457d9e3339d3d94e67aa6bab6e7804`  
		Last Modified: Mon, 31 Mar 2025 19:07:19 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:9bb39842a1562e953526ca84dade93ed7317a5171b0dd289911e3e0ef7a30d86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 KB (8851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65d8252b2336f94b11f704ef49696a12bdf9ef10309cb4154429fe3a9813fb10`

```dockerfile
```

-	Layers:
	-	`sha256:fe7adcccc05a0dc6e23afbd36ad49ea40970855eda825b6c8f4e5d3efbc4acd0`  
		Last Modified: Mon, 31 Mar 2025 19:07:19 GMT  
		Size: 8.9 KB (8851 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - linux; arm variant v7

```console
$ docker pull nats@sha256:d510696fc5434d27b38a3bd37f6e70f6baa44bb9fd974e7289f22b66efc2e532
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5881442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72773e7fdf2ee7ae0fd24dd2d85d5b015490e8b6f53959039303d91fa0b474fa`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d55862d2bf66c820eceedea01f5c750f37a0a3743706eb23a02d7a887e406432`  
		Last Modified: Mon, 31 Mar 2025 17:41:19 GMT  
		Size: 5.9 MB (5880933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4a864b46da89aef65c9bfa68ca9ddc19d2cf533aab0f916041f0ad65e2ecf91`  
		Last Modified: Mon, 31 Mar 2025 20:44:34 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:173fa1f1ea97cddff058eb5f7dcebdd162e891c9684de07fa0cf37ac0ab176eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 KB (8851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4452c75ce7d9290ef5af2fd8ddcdec5f41e40738ea2d9af9f440ee54d4e5e70b`

```dockerfile
```

-	Layers:
	-	`sha256:5e37fe48ce3230f5a30c072006fda1381fcdfb0d8e1315a2003158832930e1e8`  
		Last Modified: Mon, 31 Mar 2025 20:44:34 GMT  
		Size: 8.9 KB (8851 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:ccba147e27a60ce45bcd777a3503b578f9e04c7f99f67b306715975af0026202
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5671621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0532a34d738ab5af9a1ca292e704229198eae7ebd979105deceb2396caaa3a2c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:15097ccc819db645acfa8662d7695f5546a21829328c6c50396ba9485211e267`  
		Last Modified: Mon, 31 Mar 2025 17:41:16 GMT  
		Size: 5.7 MB (5671112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75abacb89e6aedb29f28f6a6543282c78be7ea14ffe9f9c922f9b9c68a625de5`  
		Last Modified: Mon, 31 Mar 2025 20:44:39 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:418f4f8113704b932de238f3f7349a11b57f9f7c53a2161735442632ed27d074
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 KB (8885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c76e56c7073326de47e2c39668c3db2e687270ab689412d36e2994039da940f`

```dockerfile
```

-	Layers:
	-	`sha256:6d0fde2484b74a78f8d5792ead1a410fe38808b540ff4bce2de857c4bb5956fc`  
		Last Modified: Mon, 31 Mar 2025 20:44:39 GMT  
		Size: 8.9 KB (8885 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - linux; ppc64le

```console
$ docker pull nats@sha256:6765842e0130a439bd10863a9df97feb58b4eeabd68ce848f267299a5937c269
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5649842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea3bb3296983e4335bbda6c32d55f5ee4bedf9502e5455c35c3839d382ffc34c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f74261279091b766ca91d61a1d0da2b049e137573d6cf6c41a08c2423c3b01b6`  
		Last Modified: Mon, 31 Mar 2025 17:41:19 GMT  
		Size: 5.6 MB (5649334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54d67ba201850eac96889a4cde97e3f5b08bcbbcfa7a639130f76d188af05f1d`  
		Last Modified: Mon, 31 Mar 2025 20:08:02 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:def1198eeeacc783b110cf9a6034da181107b6e8574ba497d5156006ba380960
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e09f4e3f56933cf7f0212f23c3ce591d24765edba21c35dab067620d113deead`

```dockerfile
```

-	Layers:
	-	`sha256:807bb58477341711356a934e083f272c98f30bb40237e24ef05c2dcb441e4358`  
		Last Modified: Mon, 31 Mar 2025 20:08:02 GMT  
		Size: 8.8 KB (8825 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - linux; s390x

```console
$ docker pull nats@sha256:89491c4dfa376e8d491d0ec8fc661f81fae5bd8bbc4a625df75a8e1719d4838e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6011249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e38c8d729bb9b70df3fa777383f17380382951274609f489dd8c157eb571f274`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:554b33793d1bf61783bba1ce6e69e8bbf437e2bbc9ba554ddc736994c0f14f3a`  
		Last Modified: Mon, 31 Mar 2025 17:41:19 GMT  
		Size: 6.0 MB (6010740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acab06bf1cc1c792ad42a6e5a6075275a8ec61b2b8cb88982c11fffa52a10fe3`  
		Last Modified: Mon, 31 Mar 2025 20:07:55 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:2c04eafc2d01f1cf708889883c64e880bb58ec0608442e8f63cc489942839294
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e239d5dd3821db20a0d4fefb5ab30ec06a34d7ae9cb0dc218cac71a2bc754b2e`

```dockerfile
```

-	Layers:
	-	`sha256:47f19db5270a54b41a6d54bd7788b9565227836941bb041720d91ac351c47087`  
		Last Modified: Mon, 31 Mar 2025 20:07:55 GMT  
		Size: 8.8 KB (8772 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - windows version 10.0.17763.7009; amd64

```console
$ docker pull nats@sha256:ab7eb943295ab9a492a87e24ce18ba6e5cbf72eb28aceeea8d874d0d843ec044
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 MB (113200260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68785dc79519b4e501a91713cc52804c9bfc92d6d3bb6a0ae0a04517b17a35df`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 05 Mar 2025 21:54:26 GMT
RUN Apply image 10.0.17763.7009
# Mon, 31 Mar 2025 19:15:50 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Mon, 31 Mar 2025 19:15:53 GMT
RUN cmd /S /C #(nop) COPY file:c4cf1dce77adb6c525f091c23e6d1e4cd1e3a8f732cf71d68139ef5b96fcce14 in C:\nats-server.exe 
# Mon, 31 Mar 2025 19:15:54 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Mon, 31 Mar 2025 19:15:55 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Mon, 31 Mar 2025 19:15:55 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 31 Mar 2025 19:15:56 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:543388a101bf4d470af7e8817eff3f6f3b98f13d106939ab3f507a28f2825d0a`  
		Last Modified: Tue, 11 Mar 2025 22:40:48 GMT  
		Size: 106.9 MB (106907688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c45a5f2658bc40131f0dffb2545396128f00cb7be38b1ca1991d2c0c8f8e7e6`  
		Last Modified: Mon, 31 Mar 2025 19:15:59 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e53ea45e269ae69c55545ca5506ec11cf0b476b3823db9e3a2be51833954f809`  
		Last Modified: Mon, 31 Mar 2025 19:15:59 GMT  
		Size: 6.3 MB (6286648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2127174682b07a370ad24fdd2a61d9acc90ed8b680e9558c27464fd669899159`  
		Last Modified: Mon, 31 Mar 2025 19:15:58 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9772a823cd7ce71255f3187a43ada56d0ca51566734095e257dcfa0ef4ac7a13`  
		Last Modified: Mon, 31 Mar 2025 19:15:58 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7a16678222ae598ae938ed87bc29801a0cfdcadd8babf6f1d3ce5a045b730ee`  
		Last Modified: Mon, 31 Mar 2025 19:15:58 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ccc54fd550bc0516d517f188b58982846c348a6b364c72e5c587ca687330332`  
		Last Modified: Mon, 31 Mar 2025 19:15:58 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-alpine`

```console
$ docker pull nats@sha256:ceedce1a45a9093ee13388d938dffd7a4a6d827864303bf788c830b2d7da9ec3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.10-alpine` - linux; amd64

```console
$ docker pull nats@sha256:d91fd067a47f13785d56a2fe1889af36db906927cfc8fa73b42dd8d4c5af3e12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10275908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20557405b3a6c4a60fb543b6912c045df7f628e4988f82d757816281afd4bddc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
ENV NATS_SERVER=2.10.27-binary
# Mon, 31 Mar 2025 17:39:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='2e6266b075c1f6905d974ead21ea65751125ec1f1c3a551152019755e5218c84' ;; 		armhf) natsArch='arm6'; sha256='b4f0613142539cf3260cfa6c7356dbbd3eea3020c5c01259ac7ff0af26809a86' ;; 		armv7) natsArch='arm7'; sha256='9f92594d9a3b52c2afb9ee107e168a62f1bc84a4f22defcaf8601c0a9c55bde7' ;; 		x86_64) natsArch='amd64'; sha256='5c9cd216cc0ce78092201a79e75a57607565d6e3aabad50305699dd468d579df' ;; 		x86) natsArch='386'; sha256='832a8e48a00ddccaef20602d364051d6f25790f0fc366187b1d5979b3c0cd1c9' ;; 		s390x) natsArch='s390x'; sha256='2562b3eb32a99a00dd8c9b0dfcd05d925cf1a09dd83d72268d2aa87c3f7e243f' ;; 		ppc64le) natsArch='ppc64le'; sha256='48c7d863e614224268bf98ef47b221ca43d5be00c8ce44870d819ab50ba62f2b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf2e786d87c2fb827f587f1d092a714bc1dd72caaef3c813b4cdc02d537f0b54`  
		Last Modified: Mon, 31 Mar 2025 18:43:22 GMT  
		Size: 6.6 MB (6632688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a4decf33ae70962a2b0aa91823ac92acfdb31fc46247fe4731cdb44a1902b6b`  
		Last Modified: Mon, 31 Mar 2025 18:43:22 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:244ad24672a2238fc55c73e1cce8ee6c4cf9596cf4c88286fedc665756425bfa`  
		Last Modified: Mon, 31 Mar 2025 18:43:22 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:43b0ae4493694567cf9dc6e31086ad5ca76a80ed6769ad56b784ef43582d2ee5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3e51dd3347d7350f3db959b8b414a4cd0c61d0f1fc8df0430f861dbe21ffbc3`

```dockerfile
```

-	Layers:
	-	`sha256:9d708f3d44e0fd7a4c43a87dd9350bcfbf13ba004e42e27b51fab96b6609cf78`  
		Last Modified: Mon, 31 Mar 2025 18:43:22 GMT  
		Size: 13.2 KB (13164 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:1c88b7ed8c31d9acae450b6ee0ba70603dfcef4bd4aa75a4cd469352dbf5eece
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9721157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67c6ed2d1469a463b33d4686fd103afda4f525395e49b08129df7b00f5fc2c51`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
ENV NATS_SERVER=2.10.27-binary
# Mon, 31 Mar 2025 17:39:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='2e6266b075c1f6905d974ead21ea65751125ec1f1c3a551152019755e5218c84' ;; 		armhf) natsArch='arm6'; sha256='b4f0613142539cf3260cfa6c7356dbbd3eea3020c5c01259ac7ff0af26809a86' ;; 		armv7) natsArch='arm7'; sha256='9f92594d9a3b52c2afb9ee107e168a62f1bc84a4f22defcaf8601c0a9c55bde7' ;; 		x86_64) natsArch='amd64'; sha256='5c9cd216cc0ce78092201a79e75a57607565d6e3aabad50305699dd468d579df' ;; 		x86) natsArch='386'; sha256='832a8e48a00ddccaef20602d364051d6f25790f0fc366187b1d5979b3c0cd1c9' ;; 		s390x) natsArch='s390x'; sha256='2562b3eb32a99a00dd8c9b0dfcd05d925cf1a09dd83d72268d2aa87c3f7e243f' ;; 		ppc64le) natsArch='ppc64le'; sha256='48c7d863e614224268bf98ef47b221ca43d5be00c8ce44870d819ab50ba62f2b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e60b32f3cc73ae96dd102f42cb503ec1fe5475f01e23a6307368b948dba2f95`  
		Last Modified: Mon, 31 Mar 2025 18:50:28 GMT  
		Size: 6.4 MB (6355455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7fe99ef50c87cd6c5c051ab3dbda91bd0228e982f3a88f73df6f07ef2f3a05b`  
		Last Modified: Mon, 31 Mar 2025 18:50:28 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5360439a4adf3559f65ce0640278b5bb2a72e5721a2c1cf69122f6e669dacf41`  
		Last Modified: Mon, 31 Mar 2025 18:50:28 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:c89f161f2340f184e8cd7ae1c597647a6ba8687dbfd044fb266191497a8610ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:677cfadccf63e9f9385c018644a45a24163f44b021e2fb832c15f7b355d7b4e2`

```dockerfile
```

-	Layers:
	-	`sha256:d653da947852f48b5b228b0f2fed884150d881486f718098dfa2d950ef1091ab`  
		Last Modified: Mon, 31 Mar 2025 18:50:28 GMT  
		Size: 13.2 KB (13241 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:7612892adb39fd4a90c1bfeb6d307e079c49dececfe3650bb4a52ddd8ef90840
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9443286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04ceb36059edb7f0c9e3064d6f2319c4cd12194f490d4270abd3918978225196`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
ENV NATS_SERVER=2.10.27-binary
# Mon, 31 Mar 2025 17:39:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='2e6266b075c1f6905d974ead21ea65751125ec1f1c3a551152019755e5218c84' ;; 		armhf) natsArch='arm6'; sha256='b4f0613142539cf3260cfa6c7356dbbd3eea3020c5c01259ac7ff0af26809a86' ;; 		armv7) natsArch='arm7'; sha256='9f92594d9a3b52c2afb9ee107e168a62f1bc84a4f22defcaf8601c0a9c55bde7' ;; 		x86_64) natsArch='amd64'; sha256='5c9cd216cc0ce78092201a79e75a57607565d6e3aabad50305699dd468d579df' ;; 		x86) natsArch='386'; sha256='832a8e48a00ddccaef20602d364051d6f25790f0fc366187b1d5979b3c0cd1c9' ;; 		s390x) natsArch='s390x'; sha256='2562b3eb32a99a00dd8c9b0dfcd05d925cf1a09dd83d72268d2aa87c3f7e243f' ;; 		ppc64le) natsArch='ppc64le'; sha256='48c7d863e614224268bf98ef47b221ca43d5be00c8ce44870d819ab50ba62f2b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:989ba5d675adf09ef7f3c85df22ff7e487db99578c8c747a7c2cdc69df4b0b48`  
		Last Modified: Mon, 31 Mar 2025 20:17:18 GMT  
		Size: 6.3 MB (6344193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d4cc83b0bba14f774a308fd749d95d4eb24d2c53e1f3daf9139f792e6e8e8f4`  
		Last Modified: Mon, 31 Mar 2025 20:17:17 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00e8968767ade7899dd6f1d2261ae395a772505dc8dd46d9fe9f8009272fe636`  
		Last Modified: Mon, 31 Mar 2025 20:17:17 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:4e8eff6f8a3030019aeb06f43076b35234137508736b2a7ca45986c55cdab63d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0434a25b4b4eb8af29d7ad3e5358fd54f2ee74ca3ce7b20ed3aee0a55a47c717`

```dockerfile
```

-	Layers:
	-	`sha256:a88e478f11fafa6f5da9a492bb65ed382e823530f485505f4f6d7dc0cd140e28`  
		Last Modified: Mon, 31 Mar 2025 20:17:17 GMT  
		Size: 13.2 KB (13241 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:f7745b70000cae95e9091c578eba8a67d35246979214cbd17d3b32b9d7c786ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10129644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d808ecc8d582126d78ac3ce167299e14b05f4a3320cdfa28e9b183e28e47138`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
ENV NATS_SERVER=2.10.27-binary
# Mon, 31 Mar 2025 17:39:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='2e6266b075c1f6905d974ead21ea65751125ec1f1c3a551152019755e5218c84' ;; 		armhf) natsArch='arm6'; sha256='b4f0613142539cf3260cfa6c7356dbbd3eea3020c5c01259ac7ff0af26809a86' ;; 		armv7) natsArch='arm7'; sha256='9f92594d9a3b52c2afb9ee107e168a62f1bc84a4f22defcaf8601c0a9c55bde7' ;; 		x86_64) natsArch='amd64'; sha256='5c9cd216cc0ce78092201a79e75a57607565d6e3aabad50305699dd468d579df' ;; 		x86) natsArch='386'; sha256='832a8e48a00ddccaef20602d364051d6f25790f0fc366187b1d5979b3c0cd1c9' ;; 		s390x) natsArch='s390x'; sha256='2562b3eb32a99a00dd8c9b0dfcd05d925cf1a09dd83d72268d2aa87c3f7e243f' ;; 		ppc64le) natsArch='ppc64le'; sha256='48c7d863e614224268bf98ef47b221ca43d5be00c8ce44870d819ab50ba62f2b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:230d63a94ef7c2a45a6c180e1f25b477b93358b612b10a7d11e40e3aae4c5bbe`  
		Last Modified: Mon, 31 Mar 2025 20:11:30 GMT  
		Size: 6.1 MB (6135646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe858640a1e38f916cbb792ffb2d5f4d5a50cca04aa4df41e28a8eef61469ffa`  
		Last Modified: Mon, 31 Mar 2025 20:11:29 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14179b9d744fd0fd137f41ffe02a20fb485f75f078bc73c989050cb45ddc4638`  
		Last Modified: Mon, 31 Mar 2025 20:11:29 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:9634f69d7cae51cabf75b84164263356049c0c640d9098cacc08d425efb64ddf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.3 KB (13269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3d216f1971db47ea68d38860babc7240cc3c669e7389e46bf8ca60210f84ef6`

```dockerfile
```

-	Layers:
	-	`sha256:0cadb6289bc9d43cea00aab9c172f959cead15656f80b79dc6e340b68c8517c6`  
		Last Modified: Mon, 31 Mar 2025 20:11:29 GMT  
		Size: 13.3 KB (13269 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:a0046b0100bf6d9013500535f59b164320362227c1175954755b607c19bcf4b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9688065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3ffdbad97739c36ca7f8f0dcbfac22c03553a8b1a4fc23605442e3787db313c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
ENV NATS_SERVER=2.10.27-binary
# Mon, 31 Mar 2025 17:39:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='2e6266b075c1f6905d974ead21ea65751125ec1f1c3a551152019755e5218c84' ;; 		armhf) natsArch='arm6'; sha256='b4f0613142539cf3260cfa6c7356dbbd3eea3020c5c01259ac7ff0af26809a86' ;; 		armv7) natsArch='arm7'; sha256='9f92594d9a3b52c2afb9ee107e168a62f1bc84a4f22defcaf8601c0a9c55bde7' ;; 		x86_64) natsArch='amd64'; sha256='5c9cd216cc0ce78092201a79e75a57607565d6e3aabad50305699dd468d579df' ;; 		x86) natsArch='386'; sha256='832a8e48a00ddccaef20602d364051d6f25790f0fc366187b1d5979b3c0cd1c9' ;; 		s390x) natsArch='s390x'; sha256='2562b3eb32a99a00dd8c9b0dfcd05d925cf1a09dd83d72268d2aa87c3f7e243f' ;; 		ppc64le) natsArch='ppc64le'; sha256='48c7d863e614224268bf98ef47b221ca43d5be00c8ce44870d819ab50ba62f2b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da37cd7c7eb48a58cc9fa38ca880580279f7e9d1f9b8ede411494d3a73754b55`  
		Last Modified: Mon, 31 Mar 2025 19:45:48 GMT  
		Size: 6.1 MB (6112748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:907e16a362200ce70c0989e6cc84c8b79dc59bf61737c9d928065f73bc32338e`  
		Last Modified: Mon, 31 Mar 2025 19:45:48 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55382b2ce37e5de0459bef59e902341665f6af042b1b8da495d7c08595090501`  
		Last Modified: Mon, 31 Mar 2025 19:45:48 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:b8aa897cdc47f16ba0a9794908e5dcd5a2f0b8383459a134d4f0eb1832b2f136
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f81893dc3389203506e05198be9677e9db95eb3d2dda4f3154b7908125f7248a`

```dockerfile
```

-	Layers:
	-	`sha256:2c43cc410a0fd12afe1f86896c6e689d42d0c7145867d6d9fa8da1f2bf212d61`  
		Last Modified: Mon, 31 Mar 2025 19:45:48 GMT  
		Size: 13.2 KB (13208 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; s390x

```console
$ docker pull nats@sha256:1d15bfbdae75308fe246bd9c61c8b56984a889fee63599a7855f3982bc08d445
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9941318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26e1d6acc5c00e90e93a21cf62bef4bb16e68a4c03cbf12a6551209f993a5c12`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
ENV NATS_SERVER=2.10.27-binary
# Mon, 31 Mar 2025 17:39:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='2e6266b075c1f6905d974ead21ea65751125ec1f1c3a551152019755e5218c84' ;; 		armhf) natsArch='arm6'; sha256='b4f0613142539cf3260cfa6c7356dbbd3eea3020c5c01259ac7ff0af26809a86' ;; 		armv7) natsArch='arm7'; sha256='9f92594d9a3b52c2afb9ee107e168a62f1bc84a4f22defcaf8601c0a9c55bde7' ;; 		x86_64) natsArch='amd64'; sha256='5c9cd216cc0ce78092201a79e75a57607565d6e3aabad50305699dd468d579df' ;; 		x86) natsArch='386'; sha256='832a8e48a00ddccaef20602d364051d6f25790f0fc366187b1d5979b3c0cd1c9' ;; 		s390x) natsArch='s390x'; sha256='2562b3eb32a99a00dd8c9b0dfcd05d925cf1a09dd83d72268d2aa87c3f7e243f' ;; 		ppc64le) natsArch='ppc64le'; sha256='48c7d863e614224268bf98ef47b221ca43d5be00c8ce44870d819ab50ba62f2b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0b78241f3dbd6c7cf3ceac123825e5c9e5166127edb2b9154f403670d964f76`  
		Last Modified: Mon, 31 Mar 2025 19:29:12 GMT  
		Size: 6.5 MB (6472781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf951eaa79b74dd7718f0f7978c877cebc08183b94960f9633abaeb2f5ab83bd`  
		Last Modified: Mon, 31 Mar 2025 19:29:12 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c8814e08e37e1408badb160bc7873b85c8f07409e115b507bb4344a373024c2`  
		Last Modified: Mon, 31 Mar 2025 19:29:11 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:f853c70db5824f8bec8273a1a33f4427e83c70fca2fc09bdb4e212649ab80e1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e471c0cec0a18a115b5c4538c03216ec666fd55aabad0f5b95a6cd963bfcbf5`

```dockerfile
```

-	Layers:
	-	`sha256:318aad365cfe7f993ecc3613988b3695493e344633ce75d971d7054813c7b07b`  
		Last Modified: Mon, 31 Mar 2025 19:29:11 GMT  
		Size: 13.2 KB (13164 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10-alpine3.21`

```console
$ docker pull nats@sha256:ceedce1a45a9093ee13388d938dffd7a4a6d827864303bf788c830b2d7da9ec3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.10-alpine3.21` - linux; amd64

```console
$ docker pull nats@sha256:d91fd067a47f13785d56a2fe1889af36db906927cfc8fa73b42dd8d4c5af3e12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10275908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20557405b3a6c4a60fb543b6912c045df7f628e4988f82d757816281afd4bddc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
ENV NATS_SERVER=2.10.27-binary
# Mon, 31 Mar 2025 17:39:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='2e6266b075c1f6905d974ead21ea65751125ec1f1c3a551152019755e5218c84' ;; 		armhf) natsArch='arm6'; sha256='b4f0613142539cf3260cfa6c7356dbbd3eea3020c5c01259ac7ff0af26809a86' ;; 		armv7) natsArch='arm7'; sha256='9f92594d9a3b52c2afb9ee107e168a62f1bc84a4f22defcaf8601c0a9c55bde7' ;; 		x86_64) natsArch='amd64'; sha256='5c9cd216cc0ce78092201a79e75a57607565d6e3aabad50305699dd468d579df' ;; 		x86) natsArch='386'; sha256='832a8e48a00ddccaef20602d364051d6f25790f0fc366187b1d5979b3c0cd1c9' ;; 		s390x) natsArch='s390x'; sha256='2562b3eb32a99a00dd8c9b0dfcd05d925cf1a09dd83d72268d2aa87c3f7e243f' ;; 		ppc64le) natsArch='ppc64le'; sha256='48c7d863e614224268bf98ef47b221ca43d5be00c8ce44870d819ab50ba62f2b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf2e786d87c2fb827f587f1d092a714bc1dd72caaef3c813b4cdc02d537f0b54`  
		Last Modified: Mon, 31 Mar 2025 18:43:22 GMT  
		Size: 6.6 MB (6632688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a4decf33ae70962a2b0aa91823ac92acfdb31fc46247fe4731cdb44a1902b6b`  
		Last Modified: Mon, 31 Mar 2025 18:43:22 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:244ad24672a2238fc55c73e1cce8ee6c4cf9596cf4c88286fedc665756425bfa`  
		Last Modified: Mon, 31 Mar 2025 18:43:22 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:43b0ae4493694567cf9dc6e31086ad5ca76a80ed6769ad56b784ef43582d2ee5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3e51dd3347d7350f3db959b8b414a4cd0c61d0f1fc8df0430f861dbe21ffbc3`

```dockerfile
```

-	Layers:
	-	`sha256:9d708f3d44e0fd7a4c43a87dd9350bcfbf13ba004e42e27b51fab96b6609cf78`  
		Last Modified: Mon, 31 Mar 2025 18:43:22 GMT  
		Size: 13.2 KB (13164 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.21` - linux; arm variant v6

```console
$ docker pull nats@sha256:1c88b7ed8c31d9acae450b6ee0ba70603dfcef4bd4aa75a4cd469352dbf5eece
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9721157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67c6ed2d1469a463b33d4686fd103afda4f525395e49b08129df7b00f5fc2c51`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
ENV NATS_SERVER=2.10.27-binary
# Mon, 31 Mar 2025 17:39:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='2e6266b075c1f6905d974ead21ea65751125ec1f1c3a551152019755e5218c84' ;; 		armhf) natsArch='arm6'; sha256='b4f0613142539cf3260cfa6c7356dbbd3eea3020c5c01259ac7ff0af26809a86' ;; 		armv7) natsArch='arm7'; sha256='9f92594d9a3b52c2afb9ee107e168a62f1bc84a4f22defcaf8601c0a9c55bde7' ;; 		x86_64) natsArch='amd64'; sha256='5c9cd216cc0ce78092201a79e75a57607565d6e3aabad50305699dd468d579df' ;; 		x86) natsArch='386'; sha256='832a8e48a00ddccaef20602d364051d6f25790f0fc366187b1d5979b3c0cd1c9' ;; 		s390x) natsArch='s390x'; sha256='2562b3eb32a99a00dd8c9b0dfcd05d925cf1a09dd83d72268d2aa87c3f7e243f' ;; 		ppc64le) natsArch='ppc64le'; sha256='48c7d863e614224268bf98ef47b221ca43d5be00c8ce44870d819ab50ba62f2b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e60b32f3cc73ae96dd102f42cb503ec1fe5475f01e23a6307368b948dba2f95`  
		Last Modified: Mon, 31 Mar 2025 18:50:28 GMT  
		Size: 6.4 MB (6355455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7fe99ef50c87cd6c5c051ab3dbda91bd0228e982f3a88f73df6f07ef2f3a05b`  
		Last Modified: Mon, 31 Mar 2025 18:50:28 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5360439a4adf3559f65ce0640278b5bb2a72e5721a2c1cf69122f6e669dacf41`  
		Last Modified: Mon, 31 Mar 2025 18:50:28 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:c89f161f2340f184e8cd7ae1c597647a6ba8687dbfd044fb266191497a8610ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:677cfadccf63e9f9385c018644a45a24163f44b021e2fb832c15f7b355d7b4e2`

```dockerfile
```

-	Layers:
	-	`sha256:d653da947852f48b5b228b0f2fed884150d881486f718098dfa2d950ef1091ab`  
		Last Modified: Mon, 31 Mar 2025 18:50:28 GMT  
		Size: 13.2 KB (13241 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.21` - linux; arm variant v7

```console
$ docker pull nats@sha256:7612892adb39fd4a90c1bfeb6d307e079c49dececfe3650bb4a52ddd8ef90840
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9443286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04ceb36059edb7f0c9e3064d6f2319c4cd12194f490d4270abd3918978225196`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
ENV NATS_SERVER=2.10.27-binary
# Mon, 31 Mar 2025 17:39:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='2e6266b075c1f6905d974ead21ea65751125ec1f1c3a551152019755e5218c84' ;; 		armhf) natsArch='arm6'; sha256='b4f0613142539cf3260cfa6c7356dbbd3eea3020c5c01259ac7ff0af26809a86' ;; 		armv7) natsArch='arm7'; sha256='9f92594d9a3b52c2afb9ee107e168a62f1bc84a4f22defcaf8601c0a9c55bde7' ;; 		x86_64) natsArch='amd64'; sha256='5c9cd216cc0ce78092201a79e75a57607565d6e3aabad50305699dd468d579df' ;; 		x86) natsArch='386'; sha256='832a8e48a00ddccaef20602d364051d6f25790f0fc366187b1d5979b3c0cd1c9' ;; 		s390x) natsArch='s390x'; sha256='2562b3eb32a99a00dd8c9b0dfcd05d925cf1a09dd83d72268d2aa87c3f7e243f' ;; 		ppc64le) natsArch='ppc64le'; sha256='48c7d863e614224268bf98ef47b221ca43d5be00c8ce44870d819ab50ba62f2b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:989ba5d675adf09ef7f3c85df22ff7e487db99578c8c747a7c2cdc69df4b0b48`  
		Last Modified: Mon, 31 Mar 2025 20:17:18 GMT  
		Size: 6.3 MB (6344193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d4cc83b0bba14f774a308fd749d95d4eb24d2c53e1f3daf9139f792e6e8e8f4`  
		Last Modified: Mon, 31 Mar 2025 20:17:17 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00e8968767ade7899dd6f1d2261ae395a772505dc8dd46d9fe9f8009272fe636`  
		Last Modified: Mon, 31 Mar 2025 20:17:17 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:4e8eff6f8a3030019aeb06f43076b35234137508736b2a7ca45986c55cdab63d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0434a25b4b4eb8af29d7ad3e5358fd54f2ee74ca3ce7b20ed3aee0a55a47c717`

```dockerfile
```

-	Layers:
	-	`sha256:a88e478f11fafa6f5da9a492bb65ed382e823530f485505f4f6d7dc0cd140e28`  
		Last Modified: Mon, 31 Mar 2025 20:17:17 GMT  
		Size: 13.2 KB (13241 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:f7745b70000cae95e9091c578eba8a67d35246979214cbd17d3b32b9d7c786ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10129644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d808ecc8d582126d78ac3ce167299e14b05f4a3320cdfa28e9b183e28e47138`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
ENV NATS_SERVER=2.10.27-binary
# Mon, 31 Mar 2025 17:39:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='2e6266b075c1f6905d974ead21ea65751125ec1f1c3a551152019755e5218c84' ;; 		armhf) natsArch='arm6'; sha256='b4f0613142539cf3260cfa6c7356dbbd3eea3020c5c01259ac7ff0af26809a86' ;; 		armv7) natsArch='arm7'; sha256='9f92594d9a3b52c2afb9ee107e168a62f1bc84a4f22defcaf8601c0a9c55bde7' ;; 		x86_64) natsArch='amd64'; sha256='5c9cd216cc0ce78092201a79e75a57607565d6e3aabad50305699dd468d579df' ;; 		x86) natsArch='386'; sha256='832a8e48a00ddccaef20602d364051d6f25790f0fc366187b1d5979b3c0cd1c9' ;; 		s390x) natsArch='s390x'; sha256='2562b3eb32a99a00dd8c9b0dfcd05d925cf1a09dd83d72268d2aa87c3f7e243f' ;; 		ppc64le) natsArch='ppc64le'; sha256='48c7d863e614224268bf98ef47b221ca43d5be00c8ce44870d819ab50ba62f2b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:230d63a94ef7c2a45a6c180e1f25b477b93358b612b10a7d11e40e3aae4c5bbe`  
		Last Modified: Mon, 31 Mar 2025 20:11:30 GMT  
		Size: 6.1 MB (6135646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe858640a1e38f916cbb792ffb2d5f4d5a50cca04aa4df41e28a8eef61469ffa`  
		Last Modified: Mon, 31 Mar 2025 20:11:29 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14179b9d744fd0fd137f41ffe02a20fb485f75f078bc73c989050cb45ddc4638`  
		Last Modified: Mon, 31 Mar 2025 20:11:29 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:9634f69d7cae51cabf75b84164263356049c0c640d9098cacc08d425efb64ddf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.3 KB (13269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3d216f1971db47ea68d38860babc7240cc3c669e7389e46bf8ca60210f84ef6`

```dockerfile
```

-	Layers:
	-	`sha256:0cadb6289bc9d43cea00aab9c172f959cead15656f80b79dc6e340b68c8517c6`  
		Last Modified: Mon, 31 Mar 2025 20:11:29 GMT  
		Size: 13.3 KB (13269 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.21` - linux; ppc64le

```console
$ docker pull nats@sha256:a0046b0100bf6d9013500535f59b164320362227c1175954755b607c19bcf4b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9688065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3ffdbad97739c36ca7f8f0dcbfac22c03553a8b1a4fc23605442e3787db313c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
ENV NATS_SERVER=2.10.27-binary
# Mon, 31 Mar 2025 17:39:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='2e6266b075c1f6905d974ead21ea65751125ec1f1c3a551152019755e5218c84' ;; 		armhf) natsArch='arm6'; sha256='b4f0613142539cf3260cfa6c7356dbbd3eea3020c5c01259ac7ff0af26809a86' ;; 		armv7) natsArch='arm7'; sha256='9f92594d9a3b52c2afb9ee107e168a62f1bc84a4f22defcaf8601c0a9c55bde7' ;; 		x86_64) natsArch='amd64'; sha256='5c9cd216cc0ce78092201a79e75a57607565d6e3aabad50305699dd468d579df' ;; 		x86) natsArch='386'; sha256='832a8e48a00ddccaef20602d364051d6f25790f0fc366187b1d5979b3c0cd1c9' ;; 		s390x) natsArch='s390x'; sha256='2562b3eb32a99a00dd8c9b0dfcd05d925cf1a09dd83d72268d2aa87c3f7e243f' ;; 		ppc64le) natsArch='ppc64le'; sha256='48c7d863e614224268bf98ef47b221ca43d5be00c8ce44870d819ab50ba62f2b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da37cd7c7eb48a58cc9fa38ca880580279f7e9d1f9b8ede411494d3a73754b55`  
		Last Modified: Mon, 31 Mar 2025 19:45:48 GMT  
		Size: 6.1 MB (6112748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:907e16a362200ce70c0989e6cc84c8b79dc59bf61737c9d928065f73bc32338e`  
		Last Modified: Mon, 31 Mar 2025 19:45:48 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55382b2ce37e5de0459bef59e902341665f6af042b1b8da495d7c08595090501`  
		Last Modified: Mon, 31 Mar 2025 19:45:48 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:b8aa897cdc47f16ba0a9794908e5dcd5a2f0b8383459a134d4f0eb1832b2f136
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f81893dc3389203506e05198be9677e9db95eb3d2dda4f3154b7908125f7248a`

```dockerfile
```

-	Layers:
	-	`sha256:2c43cc410a0fd12afe1f86896c6e689d42d0c7145867d6d9fa8da1f2bf212d61`  
		Last Modified: Mon, 31 Mar 2025 19:45:48 GMT  
		Size: 13.2 KB (13208 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.21` - linux; s390x

```console
$ docker pull nats@sha256:1d15bfbdae75308fe246bd9c61c8b56984a889fee63599a7855f3982bc08d445
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9941318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26e1d6acc5c00e90e93a21cf62bef4bb16e68a4c03cbf12a6551209f993a5c12`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
ENV NATS_SERVER=2.10.27-binary
# Mon, 31 Mar 2025 17:39:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='2e6266b075c1f6905d974ead21ea65751125ec1f1c3a551152019755e5218c84' ;; 		armhf) natsArch='arm6'; sha256='b4f0613142539cf3260cfa6c7356dbbd3eea3020c5c01259ac7ff0af26809a86' ;; 		armv7) natsArch='arm7'; sha256='9f92594d9a3b52c2afb9ee107e168a62f1bc84a4f22defcaf8601c0a9c55bde7' ;; 		x86_64) natsArch='amd64'; sha256='5c9cd216cc0ce78092201a79e75a57607565d6e3aabad50305699dd468d579df' ;; 		x86) natsArch='386'; sha256='832a8e48a00ddccaef20602d364051d6f25790f0fc366187b1d5979b3c0cd1c9' ;; 		s390x) natsArch='s390x'; sha256='2562b3eb32a99a00dd8c9b0dfcd05d925cf1a09dd83d72268d2aa87c3f7e243f' ;; 		ppc64le) natsArch='ppc64le'; sha256='48c7d863e614224268bf98ef47b221ca43d5be00c8ce44870d819ab50ba62f2b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0b78241f3dbd6c7cf3ceac123825e5c9e5166127edb2b9154f403670d964f76`  
		Last Modified: Mon, 31 Mar 2025 19:29:12 GMT  
		Size: 6.5 MB (6472781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf951eaa79b74dd7718f0f7978c877cebc08183b94960f9633abaeb2f5ab83bd`  
		Last Modified: Mon, 31 Mar 2025 19:29:12 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c8814e08e37e1408badb160bc7873b85c8f07409e115b507bb4344a373024c2`  
		Last Modified: Mon, 31 Mar 2025 19:29:11 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:f853c70db5824f8bec8273a1a33f4427e83c70fca2fc09bdb4e212649ab80e1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e471c0cec0a18a115b5c4538c03216ec666fd55aabad0f5b95a6cd963bfcbf5`

```dockerfile
```

-	Layers:
	-	`sha256:318aad365cfe7f993ecc3613988b3695493e344633ce75d971d7054813c7b07b`  
		Last Modified: Mon, 31 Mar 2025 19:29:11 GMT  
		Size: 13.2 KB (13164 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10-linux`

```console
$ docker pull nats@sha256:3556219cfbdaada8aa5696b2ce0583039d7846193eaf6a87c675ea5a7016c69a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.10-linux` - linux; amd64

```console
$ docker pull nats@sha256:3d3b2708e7710851a833987f3e530347d7659bba76aeace72d6f464933d57550
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6168972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65961e39279d1ae6a339ac8974109034f1ebe3d7d5a5099eaf38be54ac268706`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5b579bbe96b7482253ae3b409416bbdfaf291d6d7244c3f5fc020b18b653565a`  
		Last Modified: Mon, 31 Mar 2025 17:41:17 GMT  
		Size: 6.2 MB (6168462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:046faf28dbdb891d978b08adfc464a48ba8a6e73a4758a820994b4ce63d0b42f`  
		Last Modified: Mon, 31 Mar 2025 19:07:44 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:afe941a29e96dad9907c501b5b6787daae9cfa9146ddd8f8fd2f161684452249
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5523d84636ff676596da2cadbb6c81987810c613a7d2a05d8e427672b95674f`

```dockerfile
```

-	Layers:
	-	`sha256:acf00ab6fca0df765d7927dce65081e34a17483230da3b9fe95a04c3db26a10b`  
		Last Modified: Mon, 31 Mar 2025 19:07:44 GMT  
		Size: 8.8 KB (8771 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:3e5bffb909e76fd626bf774d58bb506d2a1101cf5d326c48fd2f9fd2b6b22df9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5892862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd79b95b8dc7a7de4ef505d7da015ccb8695dcaf721e571a5b167f50f7f8c90f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:705eaca27bc0bc30ef31a1c6ffa4e80af4a0314dcd595126dea159490cf9bc6c`  
		Last Modified: Mon, 31 Mar 2025 17:41:16 GMT  
		Size: 5.9 MB (5892354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ce9d4ac346e66940eb00e34686597227c457d9e3339d3d94e67aa6bab6e7804`  
		Last Modified: Mon, 31 Mar 2025 19:07:19 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:9bb39842a1562e953526ca84dade93ed7317a5171b0dd289911e3e0ef7a30d86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 KB (8851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65d8252b2336f94b11f704ef49696a12bdf9ef10309cb4154429fe3a9813fb10`

```dockerfile
```

-	Layers:
	-	`sha256:fe7adcccc05a0dc6e23afbd36ad49ea40970855eda825b6c8f4e5d3efbc4acd0`  
		Last Modified: Mon, 31 Mar 2025 19:07:19 GMT  
		Size: 8.9 KB (8851 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:d510696fc5434d27b38a3bd37f6e70f6baa44bb9fd974e7289f22b66efc2e532
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5881442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72773e7fdf2ee7ae0fd24dd2d85d5b015490e8b6f53959039303d91fa0b474fa`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d55862d2bf66c820eceedea01f5c750f37a0a3743706eb23a02d7a887e406432`  
		Last Modified: Mon, 31 Mar 2025 17:41:19 GMT  
		Size: 5.9 MB (5880933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4a864b46da89aef65c9bfa68ca9ddc19d2cf533aab0f916041f0ad65e2ecf91`  
		Last Modified: Mon, 31 Mar 2025 20:44:34 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:173fa1f1ea97cddff058eb5f7dcebdd162e891c9684de07fa0cf37ac0ab176eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 KB (8851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4452c75ce7d9290ef5af2fd8ddcdec5f41e40738ea2d9af9f440ee54d4e5e70b`

```dockerfile
```

-	Layers:
	-	`sha256:5e37fe48ce3230f5a30c072006fda1381fcdfb0d8e1315a2003158832930e1e8`  
		Last Modified: Mon, 31 Mar 2025 20:44:34 GMT  
		Size: 8.9 KB (8851 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:ccba147e27a60ce45bcd777a3503b578f9e04c7f99f67b306715975af0026202
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5671621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0532a34d738ab5af9a1ca292e704229198eae7ebd979105deceb2396caaa3a2c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:15097ccc819db645acfa8662d7695f5546a21829328c6c50396ba9485211e267`  
		Last Modified: Mon, 31 Mar 2025 17:41:16 GMT  
		Size: 5.7 MB (5671112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75abacb89e6aedb29f28f6a6543282c78be7ea14ffe9f9c922f9b9c68a625de5`  
		Last Modified: Mon, 31 Mar 2025 20:44:39 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:418f4f8113704b932de238f3f7349a11b57f9f7c53a2161735442632ed27d074
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 KB (8885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c76e56c7073326de47e2c39668c3db2e687270ab689412d36e2994039da940f`

```dockerfile
```

-	Layers:
	-	`sha256:6d0fde2484b74a78f8d5792ead1a410fe38808b540ff4bce2de857c4bb5956fc`  
		Last Modified: Mon, 31 Mar 2025 20:44:39 GMT  
		Size: 8.9 KB (8885 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:6765842e0130a439bd10863a9df97feb58b4eeabd68ce848f267299a5937c269
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5649842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea3bb3296983e4335bbda6c32d55f5ee4bedf9502e5455c35c3839d382ffc34c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f74261279091b766ca91d61a1d0da2b049e137573d6cf6c41a08c2423c3b01b6`  
		Last Modified: Mon, 31 Mar 2025 17:41:19 GMT  
		Size: 5.6 MB (5649334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54d67ba201850eac96889a4cde97e3f5b08bcbbcfa7a639130f76d188af05f1d`  
		Last Modified: Mon, 31 Mar 2025 20:08:02 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:def1198eeeacc783b110cf9a6034da181107b6e8574ba497d5156006ba380960
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e09f4e3f56933cf7f0212f23c3ce591d24765edba21c35dab067620d113deead`

```dockerfile
```

-	Layers:
	-	`sha256:807bb58477341711356a934e083f272c98f30bb40237e24ef05c2dcb441e4358`  
		Last Modified: Mon, 31 Mar 2025 20:08:02 GMT  
		Size: 8.8 KB (8825 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-linux` - linux; s390x

```console
$ docker pull nats@sha256:89491c4dfa376e8d491d0ec8fc661f81fae5bd8bbc4a625df75a8e1719d4838e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6011249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e38c8d729bb9b70df3fa777383f17380382951274609f489dd8c157eb571f274`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:554b33793d1bf61783bba1ce6e69e8bbf437e2bbc9ba554ddc736994c0f14f3a`  
		Last Modified: Mon, 31 Mar 2025 17:41:19 GMT  
		Size: 6.0 MB (6010740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acab06bf1cc1c792ad42a6e5a6075275a8ec61b2b8cb88982c11fffa52a10fe3`  
		Last Modified: Mon, 31 Mar 2025 20:07:55 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:2c04eafc2d01f1cf708889883c64e880bb58ec0608442e8f63cc489942839294
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e239d5dd3821db20a0d4fefb5ab30ec06a34d7ae9cb0dc218cac71a2bc754b2e`

```dockerfile
```

-	Layers:
	-	`sha256:47f19db5270a54b41a6d54bd7788b9565227836941bb041720d91ac351c47087`  
		Last Modified: Mon, 31 Mar 2025 20:07:55 GMT  
		Size: 8.8 KB (8772 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10-nanoserver`

```console
$ docker pull nats@sha256:0154aa712dd2530034925a5385fd50264ae23ab04e1237328f9e6d7cf03d7b5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `nats:2.10-nanoserver` - windows version 10.0.17763.7009; amd64

```console
$ docker pull nats@sha256:ab7eb943295ab9a492a87e24ce18ba6e5cbf72eb28aceeea8d874d0d843ec044
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 MB (113200260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68785dc79519b4e501a91713cc52804c9bfc92d6d3bb6a0ae0a04517b17a35df`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 05 Mar 2025 21:54:26 GMT
RUN Apply image 10.0.17763.7009
# Mon, 31 Mar 2025 19:15:50 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Mon, 31 Mar 2025 19:15:53 GMT
RUN cmd /S /C #(nop) COPY file:c4cf1dce77adb6c525f091c23e6d1e4cd1e3a8f732cf71d68139ef5b96fcce14 in C:\nats-server.exe 
# Mon, 31 Mar 2025 19:15:54 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Mon, 31 Mar 2025 19:15:55 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Mon, 31 Mar 2025 19:15:55 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 31 Mar 2025 19:15:56 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:543388a101bf4d470af7e8817eff3f6f3b98f13d106939ab3f507a28f2825d0a`  
		Last Modified: Tue, 11 Mar 2025 22:40:48 GMT  
		Size: 106.9 MB (106907688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c45a5f2658bc40131f0dffb2545396128f00cb7be38b1ca1991d2c0c8f8e7e6`  
		Last Modified: Mon, 31 Mar 2025 19:15:59 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e53ea45e269ae69c55545ca5506ec11cf0b476b3823db9e3a2be51833954f809`  
		Last Modified: Mon, 31 Mar 2025 19:15:59 GMT  
		Size: 6.3 MB (6286648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2127174682b07a370ad24fdd2a61d9acc90ed8b680e9558c27464fd669899159`  
		Last Modified: Mon, 31 Mar 2025 19:15:58 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9772a823cd7ce71255f3187a43ada56d0ca51566734095e257dcfa0ef4ac7a13`  
		Last Modified: Mon, 31 Mar 2025 19:15:58 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7a16678222ae598ae938ed87bc29801a0cfdcadd8babf6f1d3ce5a045b730ee`  
		Last Modified: Mon, 31 Mar 2025 19:15:58 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ccc54fd550bc0516d517f188b58982846c348a6b364c72e5c587ca687330332`  
		Last Modified: Mon, 31 Mar 2025 19:15:58 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-nanoserver-1809`

```console
$ docker pull nats@sha256:0154aa712dd2530034925a5385fd50264ae23ab04e1237328f9e6d7cf03d7b5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `nats:2.10-nanoserver-1809` - windows version 10.0.17763.7009; amd64

```console
$ docker pull nats@sha256:ab7eb943295ab9a492a87e24ce18ba6e5cbf72eb28aceeea8d874d0d843ec044
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 MB (113200260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68785dc79519b4e501a91713cc52804c9bfc92d6d3bb6a0ae0a04517b17a35df`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 05 Mar 2025 21:54:26 GMT
RUN Apply image 10.0.17763.7009
# Mon, 31 Mar 2025 19:15:50 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Mon, 31 Mar 2025 19:15:53 GMT
RUN cmd /S /C #(nop) COPY file:c4cf1dce77adb6c525f091c23e6d1e4cd1e3a8f732cf71d68139ef5b96fcce14 in C:\nats-server.exe 
# Mon, 31 Mar 2025 19:15:54 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Mon, 31 Mar 2025 19:15:55 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Mon, 31 Mar 2025 19:15:55 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 31 Mar 2025 19:15:56 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:543388a101bf4d470af7e8817eff3f6f3b98f13d106939ab3f507a28f2825d0a`  
		Last Modified: Tue, 11 Mar 2025 22:40:48 GMT  
		Size: 106.9 MB (106907688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c45a5f2658bc40131f0dffb2545396128f00cb7be38b1ca1991d2c0c8f8e7e6`  
		Last Modified: Mon, 31 Mar 2025 19:15:59 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e53ea45e269ae69c55545ca5506ec11cf0b476b3823db9e3a2be51833954f809`  
		Last Modified: Mon, 31 Mar 2025 19:15:59 GMT  
		Size: 6.3 MB (6286648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2127174682b07a370ad24fdd2a61d9acc90ed8b680e9558c27464fd669899159`  
		Last Modified: Mon, 31 Mar 2025 19:15:58 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9772a823cd7ce71255f3187a43ada56d0ca51566734095e257dcfa0ef4ac7a13`  
		Last Modified: Mon, 31 Mar 2025 19:15:58 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7a16678222ae598ae938ed87bc29801a0cfdcadd8babf6f1d3ce5a045b730ee`  
		Last Modified: Mon, 31 Mar 2025 19:15:58 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ccc54fd550bc0516d517f188b58982846c348a6b364c72e5c587ca687330332`  
		Last Modified: Mon, 31 Mar 2025 19:15:58 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-scratch`

```console
$ docker pull nats@sha256:3556219cfbdaada8aa5696b2ce0583039d7846193eaf6a87c675ea5a7016c69a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.10-scratch` - linux; amd64

```console
$ docker pull nats@sha256:3d3b2708e7710851a833987f3e530347d7659bba76aeace72d6f464933d57550
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6168972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65961e39279d1ae6a339ac8974109034f1ebe3d7d5a5099eaf38be54ac268706`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5b579bbe96b7482253ae3b409416bbdfaf291d6d7244c3f5fc020b18b653565a`  
		Last Modified: Mon, 31 Mar 2025 17:41:17 GMT  
		Size: 6.2 MB (6168462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:046faf28dbdb891d978b08adfc464a48ba8a6e73a4758a820994b4ce63d0b42f`  
		Last Modified: Mon, 31 Mar 2025 19:07:44 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:afe941a29e96dad9907c501b5b6787daae9cfa9146ddd8f8fd2f161684452249
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5523d84636ff676596da2cadbb6c81987810c613a7d2a05d8e427672b95674f`

```dockerfile
```

-	Layers:
	-	`sha256:acf00ab6fca0df765d7927dce65081e34a17483230da3b9fe95a04c3db26a10b`  
		Last Modified: Mon, 31 Mar 2025 19:07:44 GMT  
		Size: 8.8 KB (8771 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:3e5bffb909e76fd626bf774d58bb506d2a1101cf5d326c48fd2f9fd2b6b22df9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5892862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd79b95b8dc7a7de4ef505d7da015ccb8695dcaf721e571a5b167f50f7f8c90f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:705eaca27bc0bc30ef31a1c6ffa4e80af4a0314dcd595126dea159490cf9bc6c`  
		Last Modified: Mon, 31 Mar 2025 17:41:16 GMT  
		Size: 5.9 MB (5892354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ce9d4ac346e66940eb00e34686597227c457d9e3339d3d94e67aa6bab6e7804`  
		Last Modified: Mon, 31 Mar 2025 19:07:19 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:9bb39842a1562e953526ca84dade93ed7317a5171b0dd289911e3e0ef7a30d86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 KB (8851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65d8252b2336f94b11f704ef49696a12bdf9ef10309cb4154429fe3a9813fb10`

```dockerfile
```

-	Layers:
	-	`sha256:fe7adcccc05a0dc6e23afbd36ad49ea40970855eda825b6c8f4e5d3efbc4acd0`  
		Last Modified: Mon, 31 Mar 2025 19:07:19 GMT  
		Size: 8.9 KB (8851 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:d510696fc5434d27b38a3bd37f6e70f6baa44bb9fd974e7289f22b66efc2e532
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5881442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72773e7fdf2ee7ae0fd24dd2d85d5b015490e8b6f53959039303d91fa0b474fa`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d55862d2bf66c820eceedea01f5c750f37a0a3743706eb23a02d7a887e406432`  
		Last Modified: Mon, 31 Mar 2025 17:41:19 GMT  
		Size: 5.9 MB (5880933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4a864b46da89aef65c9bfa68ca9ddc19d2cf533aab0f916041f0ad65e2ecf91`  
		Last Modified: Mon, 31 Mar 2025 20:44:34 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:173fa1f1ea97cddff058eb5f7dcebdd162e891c9684de07fa0cf37ac0ab176eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 KB (8851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4452c75ce7d9290ef5af2fd8ddcdec5f41e40738ea2d9af9f440ee54d4e5e70b`

```dockerfile
```

-	Layers:
	-	`sha256:5e37fe48ce3230f5a30c072006fda1381fcdfb0d8e1315a2003158832930e1e8`  
		Last Modified: Mon, 31 Mar 2025 20:44:34 GMT  
		Size: 8.9 KB (8851 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:ccba147e27a60ce45bcd777a3503b578f9e04c7f99f67b306715975af0026202
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5671621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0532a34d738ab5af9a1ca292e704229198eae7ebd979105deceb2396caaa3a2c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:15097ccc819db645acfa8662d7695f5546a21829328c6c50396ba9485211e267`  
		Last Modified: Mon, 31 Mar 2025 17:41:16 GMT  
		Size: 5.7 MB (5671112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75abacb89e6aedb29f28f6a6543282c78be7ea14ffe9f9c922f9b9c68a625de5`  
		Last Modified: Mon, 31 Mar 2025 20:44:39 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:418f4f8113704b932de238f3f7349a11b57f9f7c53a2161735442632ed27d074
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 KB (8885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c76e56c7073326de47e2c39668c3db2e687270ab689412d36e2994039da940f`

```dockerfile
```

-	Layers:
	-	`sha256:6d0fde2484b74a78f8d5792ead1a410fe38808b540ff4bce2de857c4bb5956fc`  
		Last Modified: Mon, 31 Mar 2025 20:44:39 GMT  
		Size: 8.9 KB (8885 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:6765842e0130a439bd10863a9df97feb58b4eeabd68ce848f267299a5937c269
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5649842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea3bb3296983e4335bbda6c32d55f5ee4bedf9502e5455c35c3839d382ffc34c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f74261279091b766ca91d61a1d0da2b049e137573d6cf6c41a08c2423c3b01b6`  
		Last Modified: Mon, 31 Mar 2025 17:41:19 GMT  
		Size: 5.6 MB (5649334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54d67ba201850eac96889a4cde97e3f5b08bcbbcfa7a639130f76d188af05f1d`  
		Last Modified: Mon, 31 Mar 2025 20:08:02 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:def1198eeeacc783b110cf9a6034da181107b6e8574ba497d5156006ba380960
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e09f4e3f56933cf7f0212f23c3ce591d24765edba21c35dab067620d113deead`

```dockerfile
```

-	Layers:
	-	`sha256:807bb58477341711356a934e083f272c98f30bb40237e24ef05c2dcb441e4358`  
		Last Modified: Mon, 31 Mar 2025 20:08:02 GMT  
		Size: 8.8 KB (8825 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-scratch` - linux; s390x

```console
$ docker pull nats@sha256:89491c4dfa376e8d491d0ec8fc661f81fae5bd8bbc4a625df75a8e1719d4838e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6011249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e38c8d729bb9b70df3fa777383f17380382951274609f489dd8c157eb571f274`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:554b33793d1bf61783bba1ce6e69e8bbf437e2bbc9ba554ddc736994c0f14f3a`  
		Last Modified: Mon, 31 Mar 2025 17:41:19 GMT  
		Size: 6.0 MB (6010740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acab06bf1cc1c792ad42a6e5a6075275a8ec61b2b8cb88982c11fffa52a10fe3`  
		Last Modified: Mon, 31 Mar 2025 20:07:55 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:2c04eafc2d01f1cf708889883c64e880bb58ec0608442e8f63cc489942839294
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e239d5dd3821db20a0d4fefb5ab30ec06a34d7ae9cb0dc218cac71a2bc754b2e`

```dockerfile
```

-	Layers:
	-	`sha256:47f19db5270a54b41a6d54bd7788b9565227836941bb041720d91ac351c47087`  
		Last Modified: Mon, 31 Mar 2025 20:07:55 GMT  
		Size: 8.8 KB (8772 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10-windowsservercore`

```console
$ docker pull nats@sha256:cb5439ddd7808e051d2334b61284e985db9e29e18dac1ece11c91808f078ad9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `nats:2.10-windowsservercore` - windows version 10.0.17763.7009; amd64

```console
$ docker pull nats@sha256:81da19d8b9c3f831a0e955b72d82ae4effd3d8ce9255cbcd9954d8c28b8ee5aa
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2158620755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:663724a65768ecc751197b16012347d520d496c98f3daac85cc63636c91a8993`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 05 Mar 2025 22:09:20 GMT
RUN Install update 10.0.17763.7009
# Mon, 31 Mar 2025 18:51:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 31 Mar 2025 18:51:51 GMT
ENV NATS_DOCKERIZED=1
# Mon, 31 Mar 2025 18:51:51 GMT
ENV NATS_SERVER=2.10.27-binary
# Mon, 31 Mar 2025 18:51:52 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.27-binary/nats-server-v2.10.27-binary-windows-amd64.zip
# Mon, 31 Mar 2025 18:51:53 GMT
ENV NATS_SERVER_SHASUM=91a8ca4b87590a9915f7ccbb1064503dd2730c3c2e2b314c0ea4b59852a0c3cf
# Mon, 31 Mar 2025 18:52:44 GMT
RUN Set-PSDebug -Trace 2
# Mon, 31 Mar 2025 18:53:04 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Mon, 31 Mar 2025 18:53:05 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Mon, 31 Mar 2025 18:53:05 GMT
EXPOSE 4222 6222 8222
# Mon, 31 Mar 2025 18:53:06 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 31 Mar 2025 18:53:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77bec5e4bac3c7f6dc5d56da5ffc11e72881485b3a55330c17c915ad653f955`  
		Last Modified: Tue, 11 Mar 2025 17:48:06 GMT  
		Size: 431.4 MB (431366277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ea0b5d2f14978aab80636bdb19e438935a8e5a6b73e94108ed53021408ca032`  
		Last Modified: Mon, 31 Mar 2025 18:53:11 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81de36e26a8cba9cbcda3f5edf75fa413482a9da96b975e73aae1c5e7c7f9d6a`  
		Last Modified: Mon, 31 Mar 2025 18:53:11 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4497e248e8d2faf01244329b3ff38d1dfc686bbc87af4309800db3febdd3f539`  
		Last Modified: Mon, 31 Mar 2025 18:53:10 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecfeed092cfc0cd90939dfe8d46b6f42f6d840dbe4276c53da4f21fdcdef25ca`  
		Last Modified: Mon, 31 Mar 2025 18:53:10 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82dce49d11573a45f8a1f67135c9b2d6120595315590e1264189539c5d7b64c3`  
		Last Modified: Mon, 31 Mar 2025 18:53:10 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1f099c30d6fab9f0b5d5c9729e83af23283539ad6814bd7dd87ba4b1ef718ab`  
		Last Modified: Mon, 31 Mar 2025 18:53:10 GMT  
		Size: 334.8 KB (334804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f32db291b9a65da5a63a2e85e6a7168f70811ec460cfdf98909c3e90e9c57f9`  
		Last Modified: Mon, 31 Mar 2025 18:53:10 GMT  
		Size: 6.6 MB (6639120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:277ef5a1c99f3c0f86e6b341a1863c22fdb9ca5898f77be0f15d831586390578`  
		Last Modified: Mon, 31 Mar 2025 18:53:09 GMT  
		Size: 1.9 KB (1851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2382a37972ac8b51776422de91fdb516f966a30a68189831f3a1be1d40e796f7`  
		Last Modified: Mon, 31 Mar 2025 18:53:09 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b65adf938bdfac1a15eedf06d7c0db242c30d60b73f18362b25d749a286102ee`  
		Last Modified: Mon, 31 Mar 2025 18:53:09 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4df75bee06a36b353bd93de8413ba75114aa7214dcdf433411821ff31270233`  
		Last Modified: Mon, 31 Mar 2025 18:53:09 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-windowsservercore-1809`

```console
$ docker pull nats@sha256:cb5439ddd7808e051d2334b61284e985db9e29e18dac1ece11c91808f078ad9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `nats:2.10-windowsservercore-1809` - windows version 10.0.17763.7009; amd64

```console
$ docker pull nats@sha256:81da19d8b9c3f831a0e955b72d82ae4effd3d8ce9255cbcd9954d8c28b8ee5aa
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2158620755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:663724a65768ecc751197b16012347d520d496c98f3daac85cc63636c91a8993`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 05 Mar 2025 22:09:20 GMT
RUN Install update 10.0.17763.7009
# Mon, 31 Mar 2025 18:51:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 31 Mar 2025 18:51:51 GMT
ENV NATS_DOCKERIZED=1
# Mon, 31 Mar 2025 18:51:51 GMT
ENV NATS_SERVER=2.10.27-binary
# Mon, 31 Mar 2025 18:51:52 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.27-binary/nats-server-v2.10.27-binary-windows-amd64.zip
# Mon, 31 Mar 2025 18:51:53 GMT
ENV NATS_SERVER_SHASUM=91a8ca4b87590a9915f7ccbb1064503dd2730c3c2e2b314c0ea4b59852a0c3cf
# Mon, 31 Mar 2025 18:52:44 GMT
RUN Set-PSDebug -Trace 2
# Mon, 31 Mar 2025 18:53:04 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Mon, 31 Mar 2025 18:53:05 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Mon, 31 Mar 2025 18:53:05 GMT
EXPOSE 4222 6222 8222
# Mon, 31 Mar 2025 18:53:06 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 31 Mar 2025 18:53:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77bec5e4bac3c7f6dc5d56da5ffc11e72881485b3a55330c17c915ad653f955`  
		Last Modified: Tue, 11 Mar 2025 17:48:06 GMT  
		Size: 431.4 MB (431366277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ea0b5d2f14978aab80636bdb19e438935a8e5a6b73e94108ed53021408ca032`  
		Last Modified: Mon, 31 Mar 2025 18:53:11 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81de36e26a8cba9cbcda3f5edf75fa413482a9da96b975e73aae1c5e7c7f9d6a`  
		Last Modified: Mon, 31 Mar 2025 18:53:11 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4497e248e8d2faf01244329b3ff38d1dfc686bbc87af4309800db3febdd3f539`  
		Last Modified: Mon, 31 Mar 2025 18:53:10 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecfeed092cfc0cd90939dfe8d46b6f42f6d840dbe4276c53da4f21fdcdef25ca`  
		Last Modified: Mon, 31 Mar 2025 18:53:10 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82dce49d11573a45f8a1f67135c9b2d6120595315590e1264189539c5d7b64c3`  
		Last Modified: Mon, 31 Mar 2025 18:53:10 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1f099c30d6fab9f0b5d5c9729e83af23283539ad6814bd7dd87ba4b1ef718ab`  
		Last Modified: Mon, 31 Mar 2025 18:53:10 GMT  
		Size: 334.8 KB (334804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f32db291b9a65da5a63a2e85e6a7168f70811ec460cfdf98909c3e90e9c57f9`  
		Last Modified: Mon, 31 Mar 2025 18:53:10 GMT  
		Size: 6.6 MB (6639120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:277ef5a1c99f3c0f86e6b341a1863c22fdb9ca5898f77be0f15d831586390578`  
		Last Modified: Mon, 31 Mar 2025 18:53:09 GMT  
		Size: 1.9 KB (1851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2382a37972ac8b51776422de91fdb516f966a30a68189831f3a1be1d40e796f7`  
		Last Modified: Mon, 31 Mar 2025 18:53:09 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b65adf938bdfac1a15eedf06d7c0db242c30d60b73f18362b25d749a286102ee`  
		Last Modified: Mon, 31 Mar 2025 18:53:09 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4df75bee06a36b353bd93de8413ba75114aa7214dcdf433411821ff31270233`  
		Last Modified: Mon, 31 Mar 2025 18:53:09 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.27-binary`

```console
$ docker pull nats@sha256:383481d9952319e082c015634febccc61c74ffeb3a924bce8fdcf77f26f1b8f2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 13
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown
	-	windows version 10.0.17763.7009; amd64

### `nats:2.10.27-binary` - linux; amd64

```console
$ docker pull nats@sha256:3d3b2708e7710851a833987f3e530347d7659bba76aeace72d6f464933d57550
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6168972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65961e39279d1ae6a339ac8974109034f1ebe3d7d5a5099eaf38be54ac268706`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5b579bbe96b7482253ae3b409416bbdfaf291d6d7244c3f5fc020b18b653565a`  
		Last Modified: Mon, 31 Mar 2025 17:41:17 GMT  
		Size: 6.2 MB (6168462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:046faf28dbdb891d978b08adfc464a48ba8a6e73a4758a820994b4ce63d0b42f`  
		Last Modified: Mon, 31 Mar 2025 19:07:44 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.27-binary` - unknown; unknown

```console
$ docker pull nats@sha256:afe941a29e96dad9907c501b5b6787daae9cfa9146ddd8f8fd2f161684452249
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5523d84636ff676596da2cadbb6c81987810c613a7d2a05d8e427672b95674f`

```dockerfile
```

-	Layers:
	-	`sha256:acf00ab6fca0df765d7927dce65081e34a17483230da3b9fe95a04c3db26a10b`  
		Last Modified: Mon, 31 Mar 2025 19:07:44 GMT  
		Size: 8.8 KB (8771 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.27-binary` - linux; arm variant v6

```console
$ docker pull nats@sha256:3e5bffb909e76fd626bf774d58bb506d2a1101cf5d326c48fd2f9fd2b6b22df9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5892862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd79b95b8dc7a7de4ef505d7da015ccb8695dcaf721e571a5b167f50f7f8c90f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:705eaca27bc0bc30ef31a1c6ffa4e80af4a0314dcd595126dea159490cf9bc6c`  
		Last Modified: Mon, 31 Mar 2025 17:41:16 GMT  
		Size: 5.9 MB (5892354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ce9d4ac346e66940eb00e34686597227c457d9e3339d3d94e67aa6bab6e7804`  
		Last Modified: Mon, 31 Mar 2025 19:07:19 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.27-binary` - unknown; unknown

```console
$ docker pull nats@sha256:9bb39842a1562e953526ca84dade93ed7317a5171b0dd289911e3e0ef7a30d86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 KB (8851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65d8252b2336f94b11f704ef49696a12bdf9ef10309cb4154429fe3a9813fb10`

```dockerfile
```

-	Layers:
	-	`sha256:fe7adcccc05a0dc6e23afbd36ad49ea40970855eda825b6c8f4e5d3efbc4acd0`  
		Last Modified: Mon, 31 Mar 2025 19:07:19 GMT  
		Size: 8.9 KB (8851 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.27-binary` - linux; arm variant v7

```console
$ docker pull nats@sha256:d510696fc5434d27b38a3bd37f6e70f6baa44bb9fd974e7289f22b66efc2e532
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5881442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72773e7fdf2ee7ae0fd24dd2d85d5b015490e8b6f53959039303d91fa0b474fa`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d55862d2bf66c820eceedea01f5c750f37a0a3743706eb23a02d7a887e406432`  
		Last Modified: Mon, 31 Mar 2025 17:41:19 GMT  
		Size: 5.9 MB (5880933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4a864b46da89aef65c9bfa68ca9ddc19d2cf533aab0f916041f0ad65e2ecf91`  
		Last Modified: Mon, 31 Mar 2025 20:44:34 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.27-binary` - unknown; unknown

```console
$ docker pull nats@sha256:173fa1f1ea97cddff058eb5f7dcebdd162e891c9684de07fa0cf37ac0ab176eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 KB (8851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4452c75ce7d9290ef5af2fd8ddcdec5f41e40738ea2d9af9f440ee54d4e5e70b`

```dockerfile
```

-	Layers:
	-	`sha256:5e37fe48ce3230f5a30c072006fda1381fcdfb0d8e1315a2003158832930e1e8`  
		Last Modified: Mon, 31 Mar 2025 20:44:34 GMT  
		Size: 8.9 KB (8851 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.27-binary` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:ccba147e27a60ce45bcd777a3503b578f9e04c7f99f67b306715975af0026202
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5671621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0532a34d738ab5af9a1ca292e704229198eae7ebd979105deceb2396caaa3a2c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:15097ccc819db645acfa8662d7695f5546a21829328c6c50396ba9485211e267`  
		Last Modified: Mon, 31 Mar 2025 17:41:16 GMT  
		Size: 5.7 MB (5671112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75abacb89e6aedb29f28f6a6543282c78be7ea14ffe9f9c922f9b9c68a625de5`  
		Last Modified: Mon, 31 Mar 2025 20:44:39 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.27-binary` - unknown; unknown

```console
$ docker pull nats@sha256:418f4f8113704b932de238f3f7349a11b57f9f7c53a2161735442632ed27d074
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 KB (8885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c76e56c7073326de47e2c39668c3db2e687270ab689412d36e2994039da940f`

```dockerfile
```

-	Layers:
	-	`sha256:6d0fde2484b74a78f8d5792ead1a410fe38808b540ff4bce2de857c4bb5956fc`  
		Last Modified: Mon, 31 Mar 2025 20:44:39 GMT  
		Size: 8.9 KB (8885 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.27-binary` - linux; ppc64le

```console
$ docker pull nats@sha256:6765842e0130a439bd10863a9df97feb58b4eeabd68ce848f267299a5937c269
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5649842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea3bb3296983e4335bbda6c32d55f5ee4bedf9502e5455c35c3839d382ffc34c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f74261279091b766ca91d61a1d0da2b049e137573d6cf6c41a08c2423c3b01b6`  
		Last Modified: Mon, 31 Mar 2025 17:41:19 GMT  
		Size: 5.6 MB (5649334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54d67ba201850eac96889a4cde97e3f5b08bcbbcfa7a639130f76d188af05f1d`  
		Last Modified: Mon, 31 Mar 2025 20:08:02 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.27-binary` - unknown; unknown

```console
$ docker pull nats@sha256:def1198eeeacc783b110cf9a6034da181107b6e8574ba497d5156006ba380960
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e09f4e3f56933cf7f0212f23c3ce591d24765edba21c35dab067620d113deead`

```dockerfile
```

-	Layers:
	-	`sha256:807bb58477341711356a934e083f272c98f30bb40237e24ef05c2dcb441e4358`  
		Last Modified: Mon, 31 Mar 2025 20:08:02 GMT  
		Size: 8.8 KB (8825 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.27-binary` - linux; s390x

```console
$ docker pull nats@sha256:89491c4dfa376e8d491d0ec8fc661f81fae5bd8bbc4a625df75a8e1719d4838e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6011249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e38c8d729bb9b70df3fa777383f17380382951274609f489dd8c157eb571f274`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:554b33793d1bf61783bba1ce6e69e8bbf437e2bbc9ba554ddc736994c0f14f3a`  
		Last Modified: Mon, 31 Mar 2025 17:41:19 GMT  
		Size: 6.0 MB (6010740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acab06bf1cc1c792ad42a6e5a6075275a8ec61b2b8cb88982c11fffa52a10fe3`  
		Last Modified: Mon, 31 Mar 2025 20:07:55 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.27-binary` - unknown; unknown

```console
$ docker pull nats@sha256:2c04eafc2d01f1cf708889883c64e880bb58ec0608442e8f63cc489942839294
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e239d5dd3821db20a0d4fefb5ab30ec06a34d7ae9cb0dc218cac71a2bc754b2e`

```dockerfile
```

-	Layers:
	-	`sha256:47f19db5270a54b41a6d54bd7788b9565227836941bb041720d91ac351c47087`  
		Last Modified: Mon, 31 Mar 2025 20:07:55 GMT  
		Size: 8.8 KB (8772 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.27-binary` - windows version 10.0.17763.7009; amd64

```console
$ docker pull nats@sha256:ab7eb943295ab9a492a87e24ce18ba6e5cbf72eb28aceeea8d874d0d843ec044
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 MB (113200260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68785dc79519b4e501a91713cc52804c9bfc92d6d3bb6a0ae0a04517b17a35df`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 05 Mar 2025 21:54:26 GMT
RUN Apply image 10.0.17763.7009
# Mon, 31 Mar 2025 19:15:50 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Mon, 31 Mar 2025 19:15:53 GMT
RUN cmd /S /C #(nop) COPY file:c4cf1dce77adb6c525f091c23e6d1e4cd1e3a8f732cf71d68139ef5b96fcce14 in C:\nats-server.exe 
# Mon, 31 Mar 2025 19:15:54 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Mon, 31 Mar 2025 19:15:55 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Mon, 31 Mar 2025 19:15:55 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 31 Mar 2025 19:15:56 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:543388a101bf4d470af7e8817eff3f6f3b98f13d106939ab3f507a28f2825d0a`  
		Last Modified: Tue, 11 Mar 2025 22:40:48 GMT  
		Size: 106.9 MB (106907688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c45a5f2658bc40131f0dffb2545396128f00cb7be38b1ca1991d2c0c8f8e7e6`  
		Last Modified: Mon, 31 Mar 2025 19:15:59 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e53ea45e269ae69c55545ca5506ec11cf0b476b3823db9e3a2be51833954f809`  
		Last Modified: Mon, 31 Mar 2025 19:15:59 GMT  
		Size: 6.3 MB (6286648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2127174682b07a370ad24fdd2a61d9acc90ed8b680e9558c27464fd669899159`  
		Last Modified: Mon, 31 Mar 2025 19:15:58 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9772a823cd7ce71255f3187a43ada56d0ca51566734095e257dcfa0ef4ac7a13`  
		Last Modified: Mon, 31 Mar 2025 19:15:58 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7a16678222ae598ae938ed87bc29801a0cfdcadd8babf6f1d3ce5a045b730ee`  
		Last Modified: Mon, 31 Mar 2025 19:15:58 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ccc54fd550bc0516d517f188b58982846c348a6b364c72e5c587ca687330332`  
		Last Modified: Mon, 31 Mar 2025 19:15:58 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.27-binary-alpine`

```console
$ docker pull nats@sha256:ceedce1a45a9093ee13388d938dffd7a4a6d827864303bf788c830b2d7da9ec3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.10.27-binary-alpine` - linux; amd64

```console
$ docker pull nats@sha256:d91fd067a47f13785d56a2fe1889af36db906927cfc8fa73b42dd8d4c5af3e12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10275908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20557405b3a6c4a60fb543b6912c045df7f628e4988f82d757816281afd4bddc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
ENV NATS_SERVER=2.10.27-binary
# Mon, 31 Mar 2025 17:39:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='2e6266b075c1f6905d974ead21ea65751125ec1f1c3a551152019755e5218c84' ;; 		armhf) natsArch='arm6'; sha256='b4f0613142539cf3260cfa6c7356dbbd3eea3020c5c01259ac7ff0af26809a86' ;; 		armv7) natsArch='arm7'; sha256='9f92594d9a3b52c2afb9ee107e168a62f1bc84a4f22defcaf8601c0a9c55bde7' ;; 		x86_64) natsArch='amd64'; sha256='5c9cd216cc0ce78092201a79e75a57607565d6e3aabad50305699dd468d579df' ;; 		x86) natsArch='386'; sha256='832a8e48a00ddccaef20602d364051d6f25790f0fc366187b1d5979b3c0cd1c9' ;; 		s390x) natsArch='s390x'; sha256='2562b3eb32a99a00dd8c9b0dfcd05d925cf1a09dd83d72268d2aa87c3f7e243f' ;; 		ppc64le) natsArch='ppc64le'; sha256='48c7d863e614224268bf98ef47b221ca43d5be00c8ce44870d819ab50ba62f2b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf2e786d87c2fb827f587f1d092a714bc1dd72caaef3c813b4cdc02d537f0b54`  
		Last Modified: Mon, 31 Mar 2025 18:43:22 GMT  
		Size: 6.6 MB (6632688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a4decf33ae70962a2b0aa91823ac92acfdb31fc46247fe4731cdb44a1902b6b`  
		Last Modified: Mon, 31 Mar 2025 18:43:22 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:244ad24672a2238fc55c73e1cce8ee6c4cf9596cf4c88286fedc665756425bfa`  
		Last Modified: Mon, 31 Mar 2025 18:43:22 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.27-binary-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:43b0ae4493694567cf9dc6e31086ad5ca76a80ed6769ad56b784ef43582d2ee5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3e51dd3347d7350f3db959b8b414a4cd0c61d0f1fc8df0430f861dbe21ffbc3`

```dockerfile
```

-	Layers:
	-	`sha256:9d708f3d44e0fd7a4c43a87dd9350bcfbf13ba004e42e27b51fab96b6609cf78`  
		Last Modified: Mon, 31 Mar 2025 18:43:22 GMT  
		Size: 13.2 KB (13164 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.27-binary-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:1c88b7ed8c31d9acae450b6ee0ba70603dfcef4bd4aa75a4cd469352dbf5eece
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9721157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67c6ed2d1469a463b33d4686fd103afda4f525395e49b08129df7b00f5fc2c51`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
ENV NATS_SERVER=2.10.27-binary
# Mon, 31 Mar 2025 17:39:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='2e6266b075c1f6905d974ead21ea65751125ec1f1c3a551152019755e5218c84' ;; 		armhf) natsArch='arm6'; sha256='b4f0613142539cf3260cfa6c7356dbbd3eea3020c5c01259ac7ff0af26809a86' ;; 		armv7) natsArch='arm7'; sha256='9f92594d9a3b52c2afb9ee107e168a62f1bc84a4f22defcaf8601c0a9c55bde7' ;; 		x86_64) natsArch='amd64'; sha256='5c9cd216cc0ce78092201a79e75a57607565d6e3aabad50305699dd468d579df' ;; 		x86) natsArch='386'; sha256='832a8e48a00ddccaef20602d364051d6f25790f0fc366187b1d5979b3c0cd1c9' ;; 		s390x) natsArch='s390x'; sha256='2562b3eb32a99a00dd8c9b0dfcd05d925cf1a09dd83d72268d2aa87c3f7e243f' ;; 		ppc64le) natsArch='ppc64le'; sha256='48c7d863e614224268bf98ef47b221ca43d5be00c8ce44870d819ab50ba62f2b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e60b32f3cc73ae96dd102f42cb503ec1fe5475f01e23a6307368b948dba2f95`  
		Last Modified: Mon, 31 Mar 2025 18:50:28 GMT  
		Size: 6.4 MB (6355455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7fe99ef50c87cd6c5c051ab3dbda91bd0228e982f3a88f73df6f07ef2f3a05b`  
		Last Modified: Mon, 31 Mar 2025 18:50:28 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5360439a4adf3559f65ce0640278b5bb2a72e5721a2c1cf69122f6e669dacf41`  
		Last Modified: Mon, 31 Mar 2025 18:50:28 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.27-binary-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:c89f161f2340f184e8cd7ae1c597647a6ba8687dbfd044fb266191497a8610ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:677cfadccf63e9f9385c018644a45a24163f44b021e2fb832c15f7b355d7b4e2`

```dockerfile
```

-	Layers:
	-	`sha256:d653da947852f48b5b228b0f2fed884150d881486f718098dfa2d950ef1091ab`  
		Last Modified: Mon, 31 Mar 2025 18:50:28 GMT  
		Size: 13.2 KB (13241 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.27-binary-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:7612892adb39fd4a90c1bfeb6d307e079c49dececfe3650bb4a52ddd8ef90840
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9443286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04ceb36059edb7f0c9e3064d6f2319c4cd12194f490d4270abd3918978225196`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
ENV NATS_SERVER=2.10.27-binary
# Mon, 31 Mar 2025 17:39:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='2e6266b075c1f6905d974ead21ea65751125ec1f1c3a551152019755e5218c84' ;; 		armhf) natsArch='arm6'; sha256='b4f0613142539cf3260cfa6c7356dbbd3eea3020c5c01259ac7ff0af26809a86' ;; 		armv7) natsArch='arm7'; sha256='9f92594d9a3b52c2afb9ee107e168a62f1bc84a4f22defcaf8601c0a9c55bde7' ;; 		x86_64) natsArch='amd64'; sha256='5c9cd216cc0ce78092201a79e75a57607565d6e3aabad50305699dd468d579df' ;; 		x86) natsArch='386'; sha256='832a8e48a00ddccaef20602d364051d6f25790f0fc366187b1d5979b3c0cd1c9' ;; 		s390x) natsArch='s390x'; sha256='2562b3eb32a99a00dd8c9b0dfcd05d925cf1a09dd83d72268d2aa87c3f7e243f' ;; 		ppc64le) natsArch='ppc64le'; sha256='48c7d863e614224268bf98ef47b221ca43d5be00c8ce44870d819ab50ba62f2b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:989ba5d675adf09ef7f3c85df22ff7e487db99578c8c747a7c2cdc69df4b0b48`  
		Last Modified: Mon, 31 Mar 2025 20:17:18 GMT  
		Size: 6.3 MB (6344193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d4cc83b0bba14f774a308fd749d95d4eb24d2c53e1f3daf9139f792e6e8e8f4`  
		Last Modified: Mon, 31 Mar 2025 20:17:17 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00e8968767ade7899dd6f1d2261ae395a772505dc8dd46d9fe9f8009272fe636`  
		Last Modified: Mon, 31 Mar 2025 20:17:17 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.27-binary-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:4e8eff6f8a3030019aeb06f43076b35234137508736b2a7ca45986c55cdab63d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0434a25b4b4eb8af29d7ad3e5358fd54f2ee74ca3ce7b20ed3aee0a55a47c717`

```dockerfile
```

-	Layers:
	-	`sha256:a88e478f11fafa6f5da9a492bb65ed382e823530f485505f4f6d7dc0cd140e28`  
		Last Modified: Mon, 31 Mar 2025 20:17:17 GMT  
		Size: 13.2 KB (13241 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.27-binary-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:f7745b70000cae95e9091c578eba8a67d35246979214cbd17d3b32b9d7c786ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10129644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d808ecc8d582126d78ac3ce167299e14b05f4a3320cdfa28e9b183e28e47138`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
ENV NATS_SERVER=2.10.27-binary
# Mon, 31 Mar 2025 17:39:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='2e6266b075c1f6905d974ead21ea65751125ec1f1c3a551152019755e5218c84' ;; 		armhf) natsArch='arm6'; sha256='b4f0613142539cf3260cfa6c7356dbbd3eea3020c5c01259ac7ff0af26809a86' ;; 		armv7) natsArch='arm7'; sha256='9f92594d9a3b52c2afb9ee107e168a62f1bc84a4f22defcaf8601c0a9c55bde7' ;; 		x86_64) natsArch='amd64'; sha256='5c9cd216cc0ce78092201a79e75a57607565d6e3aabad50305699dd468d579df' ;; 		x86) natsArch='386'; sha256='832a8e48a00ddccaef20602d364051d6f25790f0fc366187b1d5979b3c0cd1c9' ;; 		s390x) natsArch='s390x'; sha256='2562b3eb32a99a00dd8c9b0dfcd05d925cf1a09dd83d72268d2aa87c3f7e243f' ;; 		ppc64le) natsArch='ppc64le'; sha256='48c7d863e614224268bf98ef47b221ca43d5be00c8ce44870d819ab50ba62f2b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:230d63a94ef7c2a45a6c180e1f25b477b93358b612b10a7d11e40e3aae4c5bbe`  
		Last Modified: Mon, 31 Mar 2025 20:11:30 GMT  
		Size: 6.1 MB (6135646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe858640a1e38f916cbb792ffb2d5f4d5a50cca04aa4df41e28a8eef61469ffa`  
		Last Modified: Mon, 31 Mar 2025 20:11:29 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14179b9d744fd0fd137f41ffe02a20fb485f75f078bc73c989050cb45ddc4638`  
		Last Modified: Mon, 31 Mar 2025 20:11:29 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.27-binary-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:9634f69d7cae51cabf75b84164263356049c0c640d9098cacc08d425efb64ddf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.3 KB (13269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3d216f1971db47ea68d38860babc7240cc3c669e7389e46bf8ca60210f84ef6`

```dockerfile
```

-	Layers:
	-	`sha256:0cadb6289bc9d43cea00aab9c172f959cead15656f80b79dc6e340b68c8517c6`  
		Last Modified: Mon, 31 Mar 2025 20:11:29 GMT  
		Size: 13.3 KB (13269 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.27-binary-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:a0046b0100bf6d9013500535f59b164320362227c1175954755b607c19bcf4b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9688065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3ffdbad97739c36ca7f8f0dcbfac22c03553a8b1a4fc23605442e3787db313c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
ENV NATS_SERVER=2.10.27-binary
# Mon, 31 Mar 2025 17:39:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='2e6266b075c1f6905d974ead21ea65751125ec1f1c3a551152019755e5218c84' ;; 		armhf) natsArch='arm6'; sha256='b4f0613142539cf3260cfa6c7356dbbd3eea3020c5c01259ac7ff0af26809a86' ;; 		armv7) natsArch='arm7'; sha256='9f92594d9a3b52c2afb9ee107e168a62f1bc84a4f22defcaf8601c0a9c55bde7' ;; 		x86_64) natsArch='amd64'; sha256='5c9cd216cc0ce78092201a79e75a57607565d6e3aabad50305699dd468d579df' ;; 		x86) natsArch='386'; sha256='832a8e48a00ddccaef20602d364051d6f25790f0fc366187b1d5979b3c0cd1c9' ;; 		s390x) natsArch='s390x'; sha256='2562b3eb32a99a00dd8c9b0dfcd05d925cf1a09dd83d72268d2aa87c3f7e243f' ;; 		ppc64le) natsArch='ppc64le'; sha256='48c7d863e614224268bf98ef47b221ca43d5be00c8ce44870d819ab50ba62f2b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da37cd7c7eb48a58cc9fa38ca880580279f7e9d1f9b8ede411494d3a73754b55`  
		Last Modified: Mon, 31 Mar 2025 19:45:48 GMT  
		Size: 6.1 MB (6112748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:907e16a362200ce70c0989e6cc84c8b79dc59bf61737c9d928065f73bc32338e`  
		Last Modified: Mon, 31 Mar 2025 19:45:48 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55382b2ce37e5de0459bef59e902341665f6af042b1b8da495d7c08595090501`  
		Last Modified: Mon, 31 Mar 2025 19:45:48 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.27-binary-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:b8aa897cdc47f16ba0a9794908e5dcd5a2f0b8383459a134d4f0eb1832b2f136
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f81893dc3389203506e05198be9677e9db95eb3d2dda4f3154b7908125f7248a`

```dockerfile
```

-	Layers:
	-	`sha256:2c43cc410a0fd12afe1f86896c6e689d42d0c7145867d6d9fa8da1f2bf212d61`  
		Last Modified: Mon, 31 Mar 2025 19:45:48 GMT  
		Size: 13.2 KB (13208 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.27-binary-alpine` - linux; s390x

```console
$ docker pull nats@sha256:1d15bfbdae75308fe246bd9c61c8b56984a889fee63599a7855f3982bc08d445
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9941318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26e1d6acc5c00e90e93a21cf62bef4bb16e68a4c03cbf12a6551209f993a5c12`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
ENV NATS_SERVER=2.10.27-binary
# Mon, 31 Mar 2025 17:39:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='2e6266b075c1f6905d974ead21ea65751125ec1f1c3a551152019755e5218c84' ;; 		armhf) natsArch='arm6'; sha256='b4f0613142539cf3260cfa6c7356dbbd3eea3020c5c01259ac7ff0af26809a86' ;; 		armv7) natsArch='arm7'; sha256='9f92594d9a3b52c2afb9ee107e168a62f1bc84a4f22defcaf8601c0a9c55bde7' ;; 		x86_64) natsArch='amd64'; sha256='5c9cd216cc0ce78092201a79e75a57607565d6e3aabad50305699dd468d579df' ;; 		x86) natsArch='386'; sha256='832a8e48a00ddccaef20602d364051d6f25790f0fc366187b1d5979b3c0cd1c9' ;; 		s390x) natsArch='s390x'; sha256='2562b3eb32a99a00dd8c9b0dfcd05d925cf1a09dd83d72268d2aa87c3f7e243f' ;; 		ppc64le) natsArch='ppc64le'; sha256='48c7d863e614224268bf98ef47b221ca43d5be00c8ce44870d819ab50ba62f2b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0b78241f3dbd6c7cf3ceac123825e5c9e5166127edb2b9154f403670d964f76`  
		Last Modified: Mon, 31 Mar 2025 19:29:12 GMT  
		Size: 6.5 MB (6472781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf951eaa79b74dd7718f0f7978c877cebc08183b94960f9633abaeb2f5ab83bd`  
		Last Modified: Mon, 31 Mar 2025 19:29:12 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c8814e08e37e1408badb160bc7873b85c8f07409e115b507bb4344a373024c2`  
		Last Modified: Mon, 31 Mar 2025 19:29:11 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.27-binary-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:f853c70db5824f8bec8273a1a33f4427e83c70fca2fc09bdb4e212649ab80e1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e471c0cec0a18a115b5c4538c03216ec666fd55aabad0f5b95a6cd963bfcbf5`

```dockerfile
```

-	Layers:
	-	`sha256:318aad365cfe7f993ecc3613988b3695493e344633ce75d971d7054813c7b07b`  
		Last Modified: Mon, 31 Mar 2025 19:29:11 GMT  
		Size: 13.2 KB (13164 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10.27-binary-alpine3.21`

```console
$ docker pull nats@sha256:ceedce1a45a9093ee13388d938dffd7a4a6d827864303bf788c830b2d7da9ec3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.10.27-binary-alpine3.21` - linux; amd64

```console
$ docker pull nats@sha256:d91fd067a47f13785d56a2fe1889af36db906927cfc8fa73b42dd8d4c5af3e12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10275908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20557405b3a6c4a60fb543b6912c045df7f628e4988f82d757816281afd4bddc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
ENV NATS_SERVER=2.10.27-binary
# Mon, 31 Mar 2025 17:39:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='2e6266b075c1f6905d974ead21ea65751125ec1f1c3a551152019755e5218c84' ;; 		armhf) natsArch='arm6'; sha256='b4f0613142539cf3260cfa6c7356dbbd3eea3020c5c01259ac7ff0af26809a86' ;; 		armv7) natsArch='arm7'; sha256='9f92594d9a3b52c2afb9ee107e168a62f1bc84a4f22defcaf8601c0a9c55bde7' ;; 		x86_64) natsArch='amd64'; sha256='5c9cd216cc0ce78092201a79e75a57607565d6e3aabad50305699dd468d579df' ;; 		x86) natsArch='386'; sha256='832a8e48a00ddccaef20602d364051d6f25790f0fc366187b1d5979b3c0cd1c9' ;; 		s390x) natsArch='s390x'; sha256='2562b3eb32a99a00dd8c9b0dfcd05d925cf1a09dd83d72268d2aa87c3f7e243f' ;; 		ppc64le) natsArch='ppc64le'; sha256='48c7d863e614224268bf98ef47b221ca43d5be00c8ce44870d819ab50ba62f2b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf2e786d87c2fb827f587f1d092a714bc1dd72caaef3c813b4cdc02d537f0b54`  
		Last Modified: Mon, 31 Mar 2025 18:43:22 GMT  
		Size: 6.6 MB (6632688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a4decf33ae70962a2b0aa91823ac92acfdb31fc46247fe4731cdb44a1902b6b`  
		Last Modified: Mon, 31 Mar 2025 18:43:22 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:244ad24672a2238fc55c73e1cce8ee6c4cf9596cf4c88286fedc665756425bfa`  
		Last Modified: Mon, 31 Mar 2025 18:43:22 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.27-binary-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:43b0ae4493694567cf9dc6e31086ad5ca76a80ed6769ad56b784ef43582d2ee5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3e51dd3347d7350f3db959b8b414a4cd0c61d0f1fc8df0430f861dbe21ffbc3`

```dockerfile
```

-	Layers:
	-	`sha256:9d708f3d44e0fd7a4c43a87dd9350bcfbf13ba004e42e27b51fab96b6609cf78`  
		Last Modified: Mon, 31 Mar 2025 18:43:22 GMT  
		Size: 13.2 KB (13164 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.27-binary-alpine3.21` - linux; arm variant v6

```console
$ docker pull nats@sha256:1c88b7ed8c31d9acae450b6ee0ba70603dfcef4bd4aa75a4cd469352dbf5eece
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9721157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67c6ed2d1469a463b33d4686fd103afda4f525395e49b08129df7b00f5fc2c51`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
ENV NATS_SERVER=2.10.27-binary
# Mon, 31 Mar 2025 17:39:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='2e6266b075c1f6905d974ead21ea65751125ec1f1c3a551152019755e5218c84' ;; 		armhf) natsArch='arm6'; sha256='b4f0613142539cf3260cfa6c7356dbbd3eea3020c5c01259ac7ff0af26809a86' ;; 		armv7) natsArch='arm7'; sha256='9f92594d9a3b52c2afb9ee107e168a62f1bc84a4f22defcaf8601c0a9c55bde7' ;; 		x86_64) natsArch='amd64'; sha256='5c9cd216cc0ce78092201a79e75a57607565d6e3aabad50305699dd468d579df' ;; 		x86) natsArch='386'; sha256='832a8e48a00ddccaef20602d364051d6f25790f0fc366187b1d5979b3c0cd1c9' ;; 		s390x) natsArch='s390x'; sha256='2562b3eb32a99a00dd8c9b0dfcd05d925cf1a09dd83d72268d2aa87c3f7e243f' ;; 		ppc64le) natsArch='ppc64le'; sha256='48c7d863e614224268bf98ef47b221ca43d5be00c8ce44870d819ab50ba62f2b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e60b32f3cc73ae96dd102f42cb503ec1fe5475f01e23a6307368b948dba2f95`  
		Last Modified: Mon, 31 Mar 2025 18:50:28 GMT  
		Size: 6.4 MB (6355455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7fe99ef50c87cd6c5c051ab3dbda91bd0228e982f3a88f73df6f07ef2f3a05b`  
		Last Modified: Mon, 31 Mar 2025 18:50:28 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5360439a4adf3559f65ce0640278b5bb2a72e5721a2c1cf69122f6e669dacf41`  
		Last Modified: Mon, 31 Mar 2025 18:50:28 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.27-binary-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:c89f161f2340f184e8cd7ae1c597647a6ba8687dbfd044fb266191497a8610ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:677cfadccf63e9f9385c018644a45a24163f44b021e2fb832c15f7b355d7b4e2`

```dockerfile
```

-	Layers:
	-	`sha256:d653da947852f48b5b228b0f2fed884150d881486f718098dfa2d950ef1091ab`  
		Last Modified: Mon, 31 Mar 2025 18:50:28 GMT  
		Size: 13.2 KB (13241 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.27-binary-alpine3.21` - linux; arm variant v7

```console
$ docker pull nats@sha256:7612892adb39fd4a90c1bfeb6d307e079c49dececfe3650bb4a52ddd8ef90840
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9443286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04ceb36059edb7f0c9e3064d6f2319c4cd12194f490d4270abd3918978225196`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
ENV NATS_SERVER=2.10.27-binary
# Mon, 31 Mar 2025 17:39:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='2e6266b075c1f6905d974ead21ea65751125ec1f1c3a551152019755e5218c84' ;; 		armhf) natsArch='arm6'; sha256='b4f0613142539cf3260cfa6c7356dbbd3eea3020c5c01259ac7ff0af26809a86' ;; 		armv7) natsArch='arm7'; sha256='9f92594d9a3b52c2afb9ee107e168a62f1bc84a4f22defcaf8601c0a9c55bde7' ;; 		x86_64) natsArch='amd64'; sha256='5c9cd216cc0ce78092201a79e75a57607565d6e3aabad50305699dd468d579df' ;; 		x86) natsArch='386'; sha256='832a8e48a00ddccaef20602d364051d6f25790f0fc366187b1d5979b3c0cd1c9' ;; 		s390x) natsArch='s390x'; sha256='2562b3eb32a99a00dd8c9b0dfcd05d925cf1a09dd83d72268d2aa87c3f7e243f' ;; 		ppc64le) natsArch='ppc64le'; sha256='48c7d863e614224268bf98ef47b221ca43d5be00c8ce44870d819ab50ba62f2b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:989ba5d675adf09ef7f3c85df22ff7e487db99578c8c747a7c2cdc69df4b0b48`  
		Last Modified: Mon, 31 Mar 2025 20:17:18 GMT  
		Size: 6.3 MB (6344193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d4cc83b0bba14f774a308fd749d95d4eb24d2c53e1f3daf9139f792e6e8e8f4`  
		Last Modified: Mon, 31 Mar 2025 20:17:17 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00e8968767ade7899dd6f1d2261ae395a772505dc8dd46d9fe9f8009272fe636`  
		Last Modified: Mon, 31 Mar 2025 20:17:17 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.27-binary-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:4e8eff6f8a3030019aeb06f43076b35234137508736b2a7ca45986c55cdab63d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0434a25b4b4eb8af29d7ad3e5358fd54f2ee74ca3ce7b20ed3aee0a55a47c717`

```dockerfile
```

-	Layers:
	-	`sha256:a88e478f11fafa6f5da9a492bb65ed382e823530f485505f4f6d7dc0cd140e28`  
		Last Modified: Mon, 31 Mar 2025 20:17:17 GMT  
		Size: 13.2 KB (13241 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.27-binary-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:f7745b70000cae95e9091c578eba8a67d35246979214cbd17d3b32b9d7c786ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10129644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d808ecc8d582126d78ac3ce167299e14b05f4a3320cdfa28e9b183e28e47138`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
ENV NATS_SERVER=2.10.27-binary
# Mon, 31 Mar 2025 17:39:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='2e6266b075c1f6905d974ead21ea65751125ec1f1c3a551152019755e5218c84' ;; 		armhf) natsArch='arm6'; sha256='b4f0613142539cf3260cfa6c7356dbbd3eea3020c5c01259ac7ff0af26809a86' ;; 		armv7) natsArch='arm7'; sha256='9f92594d9a3b52c2afb9ee107e168a62f1bc84a4f22defcaf8601c0a9c55bde7' ;; 		x86_64) natsArch='amd64'; sha256='5c9cd216cc0ce78092201a79e75a57607565d6e3aabad50305699dd468d579df' ;; 		x86) natsArch='386'; sha256='832a8e48a00ddccaef20602d364051d6f25790f0fc366187b1d5979b3c0cd1c9' ;; 		s390x) natsArch='s390x'; sha256='2562b3eb32a99a00dd8c9b0dfcd05d925cf1a09dd83d72268d2aa87c3f7e243f' ;; 		ppc64le) natsArch='ppc64le'; sha256='48c7d863e614224268bf98ef47b221ca43d5be00c8ce44870d819ab50ba62f2b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:230d63a94ef7c2a45a6c180e1f25b477b93358b612b10a7d11e40e3aae4c5bbe`  
		Last Modified: Mon, 31 Mar 2025 20:11:30 GMT  
		Size: 6.1 MB (6135646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe858640a1e38f916cbb792ffb2d5f4d5a50cca04aa4df41e28a8eef61469ffa`  
		Last Modified: Mon, 31 Mar 2025 20:11:29 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14179b9d744fd0fd137f41ffe02a20fb485f75f078bc73c989050cb45ddc4638`  
		Last Modified: Mon, 31 Mar 2025 20:11:29 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.27-binary-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:9634f69d7cae51cabf75b84164263356049c0c640d9098cacc08d425efb64ddf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.3 KB (13269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3d216f1971db47ea68d38860babc7240cc3c669e7389e46bf8ca60210f84ef6`

```dockerfile
```

-	Layers:
	-	`sha256:0cadb6289bc9d43cea00aab9c172f959cead15656f80b79dc6e340b68c8517c6`  
		Last Modified: Mon, 31 Mar 2025 20:11:29 GMT  
		Size: 13.3 KB (13269 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.27-binary-alpine3.21` - linux; ppc64le

```console
$ docker pull nats@sha256:a0046b0100bf6d9013500535f59b164320362227c1175954755b607c19bcf4b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9688065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3ffdbad97739c36ca7f8f0dcbfac22c03553a8b1a4fc23605442e3787db313c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
ENV NATS_SERVER=2.10.27-binary
# Mon, 31 Mar 2025 17:39:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='2e6266b075c1f6905d974ead21ea65751125ec1f1c3a551152019755e5218c84' ;; 		armhf) natsArch='arm6'; sha256='b4f0613142539cf3260cfa6c7356dbbd3eea3020c5c01259ac7ff0af26809a86' ;; 		armv7) natsArch='arm7'; sha256='9f92594d9a3b52c2afb9ee107e168a62f1bc84a4f22defcaf8601c0a9c55bde7' ;; 		x86_64) natsArch='amd64'; sha256='5c9cd216cc0ce78092201a79e75a57607565d6e3aabad50305699dd468d579df' ;; 		x86) natsArch='386'; sha256='832a8e48a00ddccaef20602d364051d6f25790f0fc366187b1d5979b3c0cd1c9' ;; 		s390x) natsArch='s390x'; sha256='2562b3eb32a99a00dd8c9b0dfcd05d925cf1a09dd83d72268d2aa87c3f7e243f' ;; 		ppc64le) natsArch='ppc64le'; sha256='48c7d863e614224268bf98ef47b221ca43d5be00c8ce44870d819ab50ba62f2b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da37cd7c7eb48a58cc9fa38ca880580279f7e9d1f9b8ede411494d3a73754b55`  
		Last Modified: Mon, 31 Mar 2025 19:45:48 GMT  
		Size: 6.1 MB (6112748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:907e16a362200ce70c0989e6cc84c8b79dc59bf61737c9d928065f73bc32338e`  
		Last Modified: Mon, 31 Mar 2025 19:45:48 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55382b2ce37e5de0459bef59e902341665f6af042b1b8da495d7c08595090501`  
		Last Modified: Mon, 31 Mar 2025 19:45:48 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.27-binary-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:b8aa897cdc47f16ba0a9794908e5dcd5a2f0b8383459a134d4f0eb1832b2f136
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f81893dc3389203506e05198be9677e9db95eb3d2dda4f3154b7908125f7248a`

```dockerfile
```

-	Layers:
	-	`sha256:2c43cc410a0fd12afe1f86896c6e689d42d0c7145867d6d9fa8da1f2bf212d61`  
		Last Modified: Mon, 31 Mar 2025 19:45:48 GMT  
		Size: 13.2 KB (13208 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.27-binary-alpine3.21` - linux; s390x

```console
$ docker pull nats@sha256:1d15bfbdae75308fe246bd9c61c8b56984a889fee63599a7855f3982bc08d445
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9941318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26e1d6acc5c00e90e93a21cf62bef4bb16e68a4c03cbf12a6551209f993a5c12`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
ENV NATS_SERVER=2.10.27-binary
# Mon, 31 Mar 2025 17:39:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='2e6266b075c1f6905d974ead21ea65751125ec1f1c3a551152019755e5218c84' ;; 		armhf) natsArch='arm6'; sha256='b4f0613142539cf3260cfa6c7356dbbd3eea3020c5c01259ac7ff0af26809a86' ;; 		armv7) natsArch='arm7'; sha256='9f92594d9a3b52c2afb9ee107e168a62f1bc84a4f22defcaf8601c0a9c55bde7' ;; 		x86_64) natsArch='amd64'; sha256='5c9cd216cc0ce78092201a79e75a57607565d6e3aabad50305699dd468d579df' ;; 		x86) natsArch='386'; sha256='832a8e48a00ddccaef20602d364051d6f25790f0fc366187b1d5979b3c0cd1c9' ;; 		s390x) natsArch='s390x'; sha256='2562b3eb32a99a00dd8c9b0dfcd05d925cf1a09dd83d72268d2aa87c3f7e243f' ;; 		ppc64le) natsArch='ppc64le'; sha256='48c7d863e614224268bf98ef47b221ca43d5be00c8ce44870d819ab50ba62f2b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0b78241f3dbd6c7cf3ceac123825e5c9e5166127edb2b9154f403670d964f76`  
		Last Modified: Mon, 31 Mar 2025 19:29:12 GMT  
		Size: 6.5 MB (6472781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf951eaa79b74dd7718f0f7978c877cebc08183b94960f9633abaeb2f5ab83bd`  
		Last Modified: Mon, 31 Mar 2025 19:29:12 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c8814e08e37e1408badb160bc7873b85c8f07409e115b507bb4344a373024c2`  
		Last Modified: Mon, 31 Mar 2025 19:29:11 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.27-binary-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:f853c70db5824f8bec8273a1a33f4427e83c70fca2fc09bdb4e212649ab80e1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e471c0cec0a18a115b5c4538c03216ec666fd55aabad0f5b95a6cd963bfcbf5`

```dockerfile
```

-	Layers:
	-	`sha256:318aad365cfe7f993ecc3613988b3695493e344633ce75d971d7054813c7b07b`  
		Last Modified: Mon, 31 Mar 2025 19:29:11 GMT  
		Size: 13.2 KB (13164 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10.27-binary-linux`

```console
$ docker pull nats@sha256:3556219cfbdaada8aa5696b2ce0583039d7846193eaf6a87c675ea5a7016c69a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.10.27-binary-linux` - linux; amd64

```console
$ docker pull nats@sha256:3d3b2708e7710851a833987f3e530347d7659bba76aeace72d6f464933d57550
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6168972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65961e39279d1ae6a339ac8974109034f1ebe3d7d5a5099eaf38be54ac268706`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5b579bbe96b7482253ae3b409416bbdfaf291d6d7244c3f5fc020b18b653565a`  
		Last Modified: Mon, 31 Mar 2025 17:41:17 GMT  
		Size: 6.2 MB (6168462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:046faf28dbdb891d978b08adfc464a48ba8a6e73a4758a820994b4ce63d0b42f`  
		Last Modified: Mon, 31 Mar 2025 19:07:44 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.27-binary-linux` - unknown; unknown

```console
$ docker pull nats@sha256:afe941a29e96dad9907c501b5b6787daae9cfa9146ddd8f8fd2f161684452249
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5523d84636ff676596da2cadbb6c81987810c613a7d2a05d8e427672b95674f`

```dockerfile
```

-	Layers:
	-	`sha256:acf00ab6fca0df765d7927dce65081e34a17483230da3b9fe95a04c3db26a10b`  
		Last Modified: Mon, 31 Mar 2025 19:07:44 GMT  
		Size: 8.8 KB (8771 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.27-binary-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:3e5bffb909e76fd626bf774d58bb506d2a1101cf5d326c48fd2f9fd2b6b22df9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5892862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd79b95b8dc7a7de4ef505d7da015ccb8695dcaf721e571a5b167f50f7f8c90f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:705eaca27bc0bc30ef31a1c6ffa4e80af4a0314dcd595126dea159490cf9bc6c`  
		Last Modified: Mon, 31 Mar 2025 17:41:16 GMT  
		Size: 5.9 MB (5892354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ce9d4ac346e66940eb00e34686597227c457d9e3339d3d94e67aa6bab6e7804`  
		Last Modified: Mon, 31 Mar 2025 19:07:19 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.27-binary-linux` - unknown; unknown

```console
$ docker pull nats@sha256:9bb39842a1562e953526ca84dade93ed7317a5171b0dd289911e3e0ef7a30d86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 KB (8851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65d8252b2336f94b11f704ef49696a12bdf9ef10309cb4154429fe3a9813fb10`

```dockerfile
```

-	Layers:
	-	`sha256:fe7adcccc05a0dc6e23afbd36ad49ea40970855eda825b6c8f4e5d3efbc4acd0`  
		Last Modified: Mon, 31 Mar 2025 19:07:19 GMT  
		Size: 8.9 KB (8851 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.27-binary-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:d510696fc5434d27b38a3bd37f6e70f6baa44bb9fd974e7289f22b66efc2e532
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5881442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72773e7fdf2ee7ae0fd24dd2d85d5b015490e8b6f53959039303d91fa0b474fa`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d55862d2bf66c820eceedea01f5c750f37a0a3743706eb23a02d7a887e406432`  
		Last Modified: Mon, 31 Mar 2025 17:41:19 GMT  
		Size: 5.9 MB (5880933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4a864b46da89aef65c9bfa68ca9ddc19d2cf533aab0f916041f0ad65e2ecf91`  
		Last Modified: Mon, 31 Mar 2025 20:44:34 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.27-binary-linux` - unknown; unknown

```console
$ docker pull nats@sha256:173fa1f1ea97cddff058eb5f7dcebdd162e891c9684de07fa0cf37ac0ab176eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 KB (8851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4452c75ce7d9290ef5af2fd8ddcdec5f41e40738ea2d9af9f440ee54d4e5e70b`

```dockerfile
```

-	Layers:
	-	`sha256:5e37fe48ce3230f5a30c072006fda1381fcdfb0d8e1315a2003158832930e1e8`  
		Last Modified: Mon, 31 Mar 2025 20:44:34 GMT  
		Size: 8.9 KB (8851 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.27-binary-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:ccba147e27a60ce45bcd777a3503b578f9e04c7f99f67b306715975af0026202
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5671621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0532a34d738ab5af9a1ca292e704229198eae7ebd979105deceb2396caaa3a2c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:15097ccc819db645acfa8662d7695f5546a21829328c6c50396ba9485211e267`  
		Last Modified: Mon, 31 Mar 2025 17:41:16 GMT  
		Size: 5.7 MB (5671112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75abacb89e6aedb29f28f6a6543282c78be7ea14ffe9f9c922f9b9c68a625de5`  
		Last Modified: Mon, 31 Mar 2025 20:44:39 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.27-binary-linux` - unknown; unknown

```console
$ docker pull nats@sha256:418f4f8113704b932de238f3f7349a11b57f9f7c53a2161735442632ed27d074
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 KB (8885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c76e56c7073326de47e2c39668c3db2e687270ab689412d36e2994039da940f`

```dockerfile
```

-	Layers:
	-	`sha256:6d0fde2484b74a78f8d5792ead1a410fe38808b540ff4bce2de857c4bb5956fc`  
		Last Modified: Mon, 31 Mar 2025 20:44:39 GMT  
		Size: 8.9 KB (8885 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.27-binary-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:6765842e0130a439bd10863a9df97feb58b4eeabd68ce848f267299a5937c269
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5649842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea3bb3296983e4335bbda6c32d55f5ee4bedf9502e5455c35c3839d382ffc34c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f74261279091b766ca91d61a1d0da2b049e137573d6cf6c41a08c2423c3b01b6`  
		Last Modified: Mon, 31 Mar 2025 17:41:19 GMT  
		Size: 5.6 MB (5649334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54d67ba201850eac96889a4cde97e3f5b08bcbbcfa7a639130f76d188af05f1d`  
		Last Modified: Mon, 31 Mar 2025 20:08:02 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.27-binary-linux` - unknown; unknown

```console
$ docker pull nats@sha256:def1198eeeacc783b110cf9a6034da181107b6e8574ba497d5156006ba380960
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e09f4e3f56933cf7f0212f23c3ce591d24765edba21c35dab067620d113deead`

```dockerfile
```

-	Layers:
	-	`sha256:807bb58477341711356a934e083f272c98f30bb40237e24ef05c2dcb441e4358`  
		Last Modified: Mon, 31 Mar 2025 20:08:02 GMT  
		Size: 8.8 KB (8825 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.27-binary-linux` - linux; s390x

```console
$ docker pull nats@sha256:89491c4dfa376e8d491d0ec8fc661f81fae5bd8bbc4a625df75a8e1719d4838e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6011249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e38c8d729bb9b70df3fa777383f17380382951274609f489dd8c157eb571f274`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:554b33793d1bf61783bba1ce6e69e8bbf437e2bbc9ba554ddc736994c0f14f3a`  
		Last Modified: Mon, 31 Mar 2025 17:41:19 GMT  
		Size: 6.0 MB (6010740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acab06bf1cc1c792ad42a6e5a6075275a8ec61b2b8cb88982c11fffa52a10fe3`  
		Last Modified: Mon, 31 Mar 2025 20:07:55 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.27-binary-linux` - unknown; unknown

```console
$ docker pull nats@sha256:2c04eafc2d01f1cf708889883c64e880bb58ec0608442e8f63cc489942839294
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e239d5dd3821db20a0d4fefb5ab30ec06a34d7ae9cb0dc218cac71a2bc754b2e`

```dockerfile
```

-	Layers:
	-	`sha256:47f19db5270a54b41a6d54bd7788b9565227836941bb041720d91ac351c47087`  
		Last Modified: Mon, 31 Mar 2025 20:07:55 GMT  
		Size: 8.8 KB (8772 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10.27-binary-nanoserver`

```console
$ docker pull nats@sha256:0154aa712dd2530034925a5385fd50264ae23ab04e1237328f9e6d7cf03d7b5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `nats:2.10.27-binary-nanoserver` - windows version 10.0.17763.7009; amd64

```console
$ docker pull nats@sha256:ab7eb943295ab9a492a87e24ce18ba6e5cbf72eb28aceeea8d874d0d843ec044
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 MB (113200260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68785dc79519b4e501a91713cc52804c9bfc92d6d3bb6a0ae0a04517b17a35df`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 05 Mar 2025 21:54:26 GMT
RUN Apply image 10.0.17763.7009
# Mon, 31 Mar 2025 19:15:50 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Mon, 31 Mar 2025 19:15:53 GMT
RUN cmd /S /C #(nop) COPY file:c4cf1dce77adb6c525f091c23e6d1e4cd1e3a8f732cf71d68139ef5b96fcce14 in C:\nats-server.exe 
# Mon, 31 Mar 2025 19:15:54 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Mon, 31 Mar 2025 19:15:55 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Mon, 31 Mar 2025 19:15:55 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 31 Mar 2025 19:15:56 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:543388a101bf4d470af7e8817eff3f6f3b98f13d106939ab3f507a28f2825d0a`  
		Last Modified: Tue, 11 Mar 2025 22:40:48 GMT  
		Size: 106.9 MB (106907688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c45a5f2658bc40131f0dffb2545396128f00cb7be38b1ca1991d2c0c8f8e7e6`  
		Last Modified: Mon, 31 Mar 2025 19:15:59 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e53ea45e269ae69c55545ca5506ec11cf0b476b3823db9e3a2be51833954f809`  
		Last Modified: Mon, 31 Mar 2025 19:15:59 GMT  
		Size: 6.3 MB (6286648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2127174682b07a370ad24fdd2a61d9acc90ed8b680e9558c27464fd669899159`  
		Last Modified: Mon, 31 Mar 2025 19:15:58 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9772a823cd7ce71255f3187a43ada56d0ca51566734095e257dcfa0ef4ac7a13`  
		Last Modified: Mon, 31 Mar 2025 19:15:58 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7a16678222ae598ae938ed87bc29801a0cfdcadd8babf6f1d3ce5a045b730ee`  
		Last Modified: Mon, 31 Mar 2025 19:15:58 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ccc54fd550bc0516d517f188b58982846c348a6b364c72e5c587ca687330332`  
		Last Modified: Mon, 31 Mar 2025 19:15:58 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.27-binary-nanoserver-1809`

```console
$ docker pull nats@sha256:0154aa712dd2530034925a5385fd50264ae23ab04e1237328f9e6d7cf03d7b5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `nats:2.10.27-binary-nanoserver-1809` - windows version 10.0.17763.7009; amd64

```console
$ docker pull nats@sha256:ab7eb943295ab9a492a87e24ce18ba6e5cbf72eb28aceeea8d874d0d843ec044
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 MB (113200260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68785dc79519b4e501a91713cc52804c9bfc92d6d3bb6a0ae0a04517b17a35df`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 05 Mar 2025 21:54:26 GMT
RUN Apply image 10.0.17763.7009
# Mon, 31 Mar 2025 19:15:50 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Mon, 31 Mar 2025 19:15:53 GMT
RUN cmd /S /C #(nop) COPY file:c4cf1dce77adb6c525f091c23e6d1e4cd1e3a8f732cf71d68139ef5b96fcce14 in C:\nats-server.exe 
# Mon, 31 Mar 2025 19:15:54 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Mon, 31 Mar 2025 19:15:55 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Mon, 31 Mar 2025 19:15:55 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 31 Mar 2025 19:15:56 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:543388a101bf4d470af7e8817eff3f6f3b98f13d106939ab3f507a28f2825d0a`  
		Last Modified: Tue, 11 Mar 2025 22:40:48 GMT  
		Size: 106.9 MB (106907688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c45a5f2658bc40131f0dffb2545396128f00cb7be38b1ca1991d2c0c8f8e7e6`  
		Last Modified: Mon, 31 Mar 2025 19:15:59 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e53ea45e269ae69c55545ca5506ec11cf0b476b3823db9e3a2be51833954f809`  
		Last Modified: Mon, 31 Mar 2025 19:15:59 GMT  
		Size: 6.3 MB (6286648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2127174682b07a370ad24fdd2a61d9acc90ed8b680e9558c27464fd669899159`  
		Last Modified: Mon, 31 Mar 2025 19:15:58 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9772a823cd7ce71255f3187a43ada56d0ca51566734095e257dcfa0ef4ac7a13`  
		Last Modified: Mon, 31 Mar 2025 19:15:58 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7a16678222ae598ae938ed87bc29801a0cfdcadd8babf6f1d3ce5a045b730ee`  
		Last Modified: Mon, 31 Mar 2025 19:15:58 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ccc54fd550bc0516d517f188b58982846c348a6b364c72e5c587ca687330332`  
		Last Modified: Mon, 31 Mar 2025 19:15:58 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.27-binary-scratch`

```console
$ docker pull nats@sha256:3556219cfbdaada8aa5696b2ce0583039d7846193eaf6a87c675ea5a7016c69a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.10.27-binary-scratch` - linux; amd64

```console
$ docker pull nats@sha256:3d3b2708e7710851a833987f3e530347d7659bba76aeace72d6f464933d57550
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6168972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65961e39279d1ae6a339ac8974109034f1ebe3d7d5a5099eaf38be54ac268706`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5b579bbe96b7482253ae3b409416bbdfaf291d6d7244c3f5fc020b18b653565a`  
		Last Modified: Mon, 31 Mar 2025 17:41:17 GMT  
		Size: 6.2 MB (6168462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:046faf28dbdb891d978b08adfc464a48ba8a6e73a4758a820994b4ce63d0b42f`  
		Last Modified: Mon, 31 Mar 2025 19:07:44 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.27-binary-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:afe941a29e96dad9907c501b5b6787daae9cfa9146ddd8f8fd2f161684452249
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5523d84636ff676596da2cadbb6c81987810c613a7d2a05d8e427672b95674f`

```dockerfile
```

-	Layers:
	-	`sha256:acf00ab6fca0df765d7927dce65081e34a17483230da3b9fe95a04c3db26a10b`  
		Last Modified: Mon, 31 Mar 2025 19:07:44 GMT  
		Size: 8.8 KB (8771 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.27-binary-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:3e5bffb909e76fd626bf774d58bb506d2a1101cf5d326c48fd2f9fd2b6b22df9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5892862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd79b95b8dc7a7de4ef505d7da015ccb8695dcaf721e571a5b167f50f7f8c90f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:705eaca27bc0bc30ef31a1c6ffa4e80af4a0314dcd595126dea159490cf9bc6c`  
		Last Modified: Mon, 31 Mar 2025 17:41:16 GMT  
		Size: 5.9 MB (5892354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ce9d4ac346e66940eb00e34686597227c457d9e3339d3d94e67aa6bab6e7804`  
		Last Modified: Mon, 31 Mar 2025 19:07:19 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.27-binary-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:9bb39842a1562e953526ca84dade93ed7317a5171b0dd289911e3e0ef7a30d86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 KB (8851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65d8252b2336f94b11f704ef49696a12bdf9ef10309cb4154429fe3a9813fb10`

```dockerfile
```

-	Layers:
	-	`sha256:fe7adcccc05a0dc6e23afbd36ad49ea40970855eda825b6c8f4e5d3efbc4acd0`  
		Last Modified: Mon, 31 Mar 2025 19:07:19 GMT  
		Size: 8.9 KB (8851 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.27-binary-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:d510696fc5434d27b38a3bd37f6e70f6baa44bb9fd974e7289f22b66efc2e532
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5881442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72773e7fdf2ee7ae0fd24dd2d85d5b015490e8b6f53959039303d91fa0b474fa`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d55862d2bf66c820eceedea01f5c750f37a0a3743706eb23a02d7a887e406432`  
		Last Modified: Mon, 31 Mar 2025 17:41:19 GMT  
		Size: 5.9 MB (5880933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4a864b46da89aef65c9bfa68ca9ddc19d2cf533aab0f916041f0ad65e2ecf91`  
		Last Modified: Mon, 31 Mar 2025 20:44:34 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.27-binary-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:173fa1f1ea97cddff058eb5f7dcebdd162e891c9684de07fa0cf37ac0ab176eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 KB (8851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4452c75ce7d9290ef5af2fd8ddcdec5f41e40738ea2d9af9f440ee54d4e5e70b`

```dockerfile
```

-	Layers:
	-	`sha256:5e37fe48ce3230f5a30c072006fda1381fcdfb0d8e1315a2003158832930e1e8`  
		Last Modified: Mon, 31 Mar 2025 20:44:34 GMT  
		Size: 8.9 KB (8851 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.27-binary-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:ccba147e27a60ce45bcd777a3503b578f9e04c7f99f67b306715975af0026202
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5671621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0532a34d738ab5af9a1ca292e704229198eae7ebd979105deceb2396caaa3a2c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:15097ccc819db645acfa8662d7695f5546a21829328c6c50396ba9485211e267`  
		Last Modified: Mon, 31 Mar 2025 17:41:16 GMT  
		Size: 5.7 MB (5671112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75abacb89e6aedb29f28f6a6543282c78be7ea14ffe9f9c922f9b9c68a625de5`  
		Last Modified: Mon, 31 Mar 2025 20:44:39 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.27-binary-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:418f4f8113704b932de238f3f7349a11b57f9f7c53a2161735442632ed27d074
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 KB (8885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c76e56c7073326de47e2c39668c3db2e687270ab689412d36e2994039da940f`

```dockerfile
```

-	Layers:
	-	`sha256:6d0fde2484b74a78f8d5792ead1a410fe38808b540ff4bce2de857c4bb5956fc`  
		Last Modified: Mon, 31 Mar 2025 20:44:39 GMT  
		Size: 8.9 KB (8885 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.27-binary-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:6765842e0130a439bd10863a9df97feb58b4eeabd68ce848f267299a5937c269
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5649842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea3bb3296983e4335bbda6c32d55f5ee4bedf9502e5455c35c3839d382ffc34c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f74261279091b766ca91d61a1d0da2b049e137573d6cf6c41a08c2423c3b01b6`  
		Last Modified: Mon, 31 Mar 2025 17:41:19 GMT  
		Size: 5.6 MB (5649334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54d67ba201850eac96889a4cde97e3f5b08bcbbcfa7a639130f76d188af05f1d`  
		Last Modified: Mon, 31 Mar 2025 20:08:02 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.27-binary-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:def1198eeeacc783b110cf9a6034da181107b6e8574ba497d5156006ba380960
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e09f4e3f56933cf7f0212f23c3ce591d24765edba21c35dab067620d113deead`

```dockerfile
```

-	Layers:
	-	`sha256:807bb58477341711356a934e083f272c98f30bb40237e24ef05c2dcb441e4358`  
		Last Modified: Mon, 31 Mar 2025 20:08:02 GMT  
		Size: 8.8 KB (8825 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.27-binary-scratch` - linux; s390x

```console
$ docker pull nats@sha256:89491c4dfa376e8d491d0ec8fc661f81fae5bd8bbc4a625df75a8e1719d4838e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6011249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e38c8d729bb9b70df3fa777383f17380382951274609f489dd8c157eb571f274`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:554b33793d1bf61783bba1ce6e69e8bbf437e2bbc9ba554ddc736994c0f14f3a`  
		Last Modified: Mon, 31 Mar 2025 17:41:19 GMT  
		Size: 6.0 MB (6010740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acab06bf1cc1c792ad42a6e5a6075275a8ec61b2b8cb88982c11fffa52a10fe3`  
		Last Modified: Mon, 31 Mar 2025 20:07:55 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.27-binary-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:2c04eafc2d01f1cf708889883c64e880bb58ec0608442e8f63cc489942839294
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e239d5dd3821db20a0d4fefb5ab30ec06a34d7ae9cb0dc218cac71a2bc754b2e`

```dockerfile
```

-	Layers:
	-	`sha256:47f19db5270a54b41a6d54bd7788b9565227836941bb041720d91ac351c47087`  
		Last Modified: Mon, 31 Mar 2025 20:07:55 GMT  
		Size: 8.8 KB (8772 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10.27-binary-windowsservercore`

```console
$ docker pull nats@sha256:cb5439ddd7808e051d2334b61284e985db9e29e18dac1ece11c91808f078ad9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `nats:2.10.27-binary-windowsservercore` - windows version 10.0.17763.7009; amd64

```console
$ docker pull nats@sha256:81da19d8b9c3f831a0e955b72d82ae4effd3d8ce9255cbcd9954d8c28b8ee5aa
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2158620755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:663724a65768ecc751197b16012347d520d496c98f3daac85cc63636c91a8993`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 05 Mar 2025 22:09:20 GMT
RUN Install update 10.0.17763.7009
# Mon, 31 Mar 2025 18:51:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 31 Mar 2025 18:51:51 GMT
ENV NATS_DOCKERIZED=1
# Mon, 31 Mar 2025 18:51:51 GMT
ENV NATS_SERVER=2.10.27-binary
# Mon, 31 Mar 2025 18:51:52 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.27-binary/nats-server-v2.10.27-binary-windows-amd64.zip
# Mon, 31 Mar 2025 18:51:53 GMT
ENV NATS_SERVER_SHASUM=91a8ca4b87590a9915f7ccbb1064503dd2730c3c2e2b314c0ea4b59852a0c3cf
# Mon, 31 Mar 2025 18:52:44 GMT
RUN Set-PSDebug -Trace 2
# Mon, 31 Mar 2025 18:53:04 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Mon, 31 Mar 2025 18:53:05 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Mon, 31 Mar 2025 18:53:05 GMT
EXPOSE 4222 6222 8222
# Mon, 31 Mar 2025 18:53:06 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 31 Mar 2025 18:53:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77bec5e4bac3c7f6dc5d56da5ffc11e72881485b3a55330c17c915ad653f955`  
		Last Modified: Tue, 11 Mar 2025 17:48:06 GMT  
		Size: 431.4 MB (431366277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ea0b5d2f14978aab80636bdb19e438935a8e5a6b73e94108ed53021408ca032`  
		Last Modified: Mon, 31 Mar 2025 18:53:11 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81de36e26a8cba9cbcda3f5edf75fa413482a9da96b975e73aae1c5e7c7f9d6a`  
		Last Modified: Mon, 31 Mar 2025 18:53:11 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4497e248e8d2faf01244329b3ff38d1dfc686bbc87af4309800db3febdd3f539`  
		Last Modified: Mon, 31 Mar 2025 18:53:10 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecfeed092cfc0cd90939dfe8d46b6f42f6d840dbe4276c53da4f21fdcdef25ca`  
		Last Modified: Mon, 31 Mar 2025 18:53:10 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82dce49d11573a45f8a1f67135c9b2d6120595315590e1264189539c5d7b64c3`  
		Last Modified: Mon, 31 Mar 2025 18:53:10 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1f099c30d6fab9f0b5d5c9729e83af23283539ad6814bd7dd87ba4b1ef718ab`  
		Last Modified: Mon, 31 Mar 2025 18:53:10 GMT  
		Size: 334.8 KB (334804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f32db291b9a65da5a63a2e85e6a7168f70811ec460cfdf98909c3e90e9c57f9`  
		Last Modified: Mon, 31 Mar 2025 18:53:10 GMT  
		Size: 6.6 MB (6639120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:277ef5a1c99f3c0f86e6b341a1863c22fdb9ca5898f77be0f15d831586390578`  
		Last Modified: Mon, 31 Mar 2025 18:53:09 GMT  
		Size: 1.9 KB (1851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2382a37972ac8b51776422de91fdb516f966a30a68189831f3a1be1d40e796f7`  
		Last Modified: Mon, 31 Mar 2025 18:53:09 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b65adf938bdfac1a15eedf06d7c0db242c30d60b73f18362b25d749a286102ee`  
		Last Modified: Mon, 31 Mar 2025 18:53:09 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4df75bee06a36b353bd93de8413ba75114aa7214dcdf433411821ff31270233`  
		Last Modified: Mon, 31 Mar 2025 18:53:09 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.27-binary-windowsservercore-1809`

```console
$ docker pull nats@sha256:cb5439ddd7808e051d2334b61284e985db9e29e18dac1ece11c91808f078ad9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `nats:2.10.27-binary-windowsservercore-1809` - windows version 10.0.17763.7009; amd64

```console
$ docker pull nats@sha256:81da19d8b9c3f831a0e955b72d82ae4effd3d8ce9255cbcd9954d8c28b8ee5aa
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2158620755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:663724a65768ecc751197b16012347d520d496c98f3daac85cc63636c91a8993`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 05 Mar 2025 22:09:20 GMT
RUN Install update 10.0.17763.7009
# Mon, 31 Mar 2025 18:51:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 31 Mar 2025 18:51:51 GMT
ENV NATS_DOCKERIZED=1
# Mon, 31 Mar 2025 18:51:51 GMT
ENV NATS_SERVER=2.10.27-binary
# Mon, 31 Mar 2025 18:51:52 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.27-binary/nats-server-v2.10.27-binary-windows-amd64.zip
# Mon, 31 Mar 2025 18:51:53 GMT
ENV NATS_SERVER_SHASUM=91a8ca4b87590a9915f7ccbb1064503dd2730c3c2e2b314c0ea4b59852a0c3cf
# Mon, 31 Mar 2025 18:52:44 GMT
RUN Set-PSDebug -Trace 2
# Mon, 31 Mar 2025 18:53:04 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Mon, 31 Mar 2025 18:53:05 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Mon, 31 Mar 2025 18:53:05 GMT
EXPOSE 4222 6222 8222
# Mon, 31 Mar 2025 18:53:06 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 31 Mar 2025 18:53:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77bec5e4bac3c7f6dc5d56da5ffc11e72881485b3a55330c17c915ad653f955`  
		Last Modified: Tue, 11 Mar 2025 17:48:06 GMT  
		Size: 431.4 MB (431366277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ea0b5d2f14978aab80636bdb19e438935a8e5a6b73e94108ed53021408ca032`  
		Last Modified: Mon, 31 Mar 2025 18:53:11 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81de36e26a8cba9cbcda3f5edf75fa413482a9da96b975e73aae1c5e7c7f9d6a`  
		Last Modified: Mon, 31 Mar 2025 18:53:11 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4497e248e8d2faf01244329b3ff38d1dfc686bbc87af4309800db3febdd3f539`  
		Last Modified: Mon, 31 Mar 2025 18:53:10 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecfeed092cfc0cd90939dfe8d46b6f42f6d840dbe4276c53da4f21fdcdef25ca`  
		Last Modified: Mon, 31 Mar 2025 18:53:10 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82dce49d11573a45f8a1f67135c9b2d6120595315590e1264189539c5d7b64c3`  
		Last Modified: Mon, 31 Mar 2025 18:53:10 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1f099c30d6fab9f0b5d5c9729e83af23283539ad6814bd7dd87ba4b1ef718ab`  
		Last Modified: Mon, 31 Mar 2025 18:53:10 GMT  
		Size: 334.8 KB (334804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f32db291b9a65da5a63a2e85e6a7168f70811ec460cfdf98909c3e90e9c57f9`  
		Last Modified: Mon, 31 Mar 2025 18:53:10 GMT  
		Size: 6.6 MB (6639120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:277ef5a1c99f3c0f86e6b341a1863c22fdb9ca5898f77be0f15d831586390578`  
		Last Modified: Mon, 31 Mar 2025 18:53:09 GMT  
		Size: 1.9 KB (1851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2382a37972ac8b51776422de91fdb516f966a30a68189831f3a1be1d40e796f7`  
		Last Modified: Mon, 31 Mar 2025 18:53:09 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b65adf938bdfac1a15eedf06d7c0db242c30d60b73f18362b25d749a286102ee`  
		Last Modified: Mon, 31 Mar 2025 18:53:09 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4df75bee06a36b353bd93de8413ba75114aa7214dcdf433411821ff31270233`  
		Last Modified: Mon, 31 Mar 2025 18:53:09 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11`

```console
$ docker pull nats@sha256:76fe53997736051e3511ddc26d585abd679fe3a30dbf74d19418bb0035fde031
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 13
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown
	-	windows version 10.0.17763.7009; amd64

### `nats:2.11` - linux; amd64

```console
$ docker pull nats@sha256:0b313c16824b8d98736c06153fa01af3c8d62eebc6298e9062fd2e00c0a3e865
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6282666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5a2333da61b6c9f0de1de8235aca52ee071283b0c8c6487d3ea15b4a0f9f8e2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:54120e60f5a574cbbfd83de2711330ae98499a27ff592bdb694994b87749dd23`  
		Last Modified: Mon, 31 Mar 2025 17:41:30 GMT  
		Size: 6.3 MB (6282155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71d71c31c70e45e814d8db85102321f1459be653c595cd91fafb76306cdf405e`  
		Last Modified: Mon, 31 Mar 2025 19:07:36 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11` - unknown; unknown

```console
$ docker pull nats@sha256:b8d62bc797363d5eab76aea96ec144d02b901da4dba8eb8bf31cc4e51e3a09d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbd51cd5b25ea5c4355cd2cde0e286d4f6da98802af9ed8b477001ff7ece4679`

```dockerfile
```

-	Layers:
	-	`sha256:19abc39a4cbb247bfa12363ce59bbce1e3bf861fddb9055c3a17e2d39d54d204`  
		Last Modified: Mon, 31 Mar 2025 19:07:36 GMT  
		Size: 10.5 KB (10523 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11` - linux; arm variant v6

```console
$ docker pull nats@sha256:af5758489c2981e0a1028dc47f82f0dd2d26e2fac7ac1e478a2a15a12029f6d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6002169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c17f13cf88d7cb6d029eafd34cd847cbacebb2131dc5b7ecfbed791e2958e6a4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:098bda892a4e7ddd77ca838f72ef9757e9b3cfae3c7bc97076a8dd0b6fd92597`  
		Last Modified: Mon, 31 Mar 2025 17:41:30 GMT  
		Size: 6.0 MB (6001660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff1d2651842734b21329c25e1004a4da19102e57001381e60bb4fd58723fe19`  
		Last Modified: Mon, 31 Mar 2025 19:07:08 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11` - unknown; unknown

```console
$ docker pull nats@sha256:736b8ee8472809de9731d9c426d2113e533e5ac68c9fbf4cd6bb44eb636b3d79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ffa52afcf9f827961f6f692daeb94f398721ac7559f559d56147558f6742150`

```dockerfile
```

-	Layers:
	-	`sha256:cc5887e8b88d73925b5364f9143ca37566f003a1560dffe173f7be8f10d66806`  
		Last Modified: Mon, 31 Mar 2025 19:07:08 GMT  
		Size: 10.7 KB (10650 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11` - linux; arm variant v7

```console
$ docker pull nats@sha256:f1752b6d8b3a5506fab1fdf93ce66a6bd6e934d33a3c230231458f254ff505a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5992492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68d3d700cbec0d68868397c08f331e9cee8a3e484035ab651de2414c1bc1039b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7ae07ef7aadc186e26516a3b1a5bacd27b42c41b8d63efc540622587ef29be07`  
		Last Modified: Mon, 31 Mar 2025 17:41:36 GMT  
		Size: 6.0 MB (5991983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d132fb7bc19f6f368e535b5a46903e88d661e5c0f5e33c79b7d66b962039598`  
		Last Modified: Mon, 31 Mar 2025 20:44:23 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11` - unknown; unknown

```console
$ docker pull nats@sha256:ff00ada993e928a0dbcd0e627e845b5f9c4d11042f0e089912b8ef2969c89876
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab26b373d46f30d56fc9b9ecf02d3c518eb5ab041a8fbb69e562b49b1a864d9d`

```dockerfile
```

-	Layers:
	-	`sha256:d552b4d64ce37965149a8aaeed3a0eebd251066efc77cb63ad2307f9d0bbdef7`  
		Last Modified: Mon, 31 Mar 2025 20:44:23 GMT  
		Size: 10.6 KB (10649 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a360fbbfeb6f19012e875675cf70ea15e5ea3d9e003d5ccf1a61adeed8d515c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5776951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aad8d86003a865c09c995830bd52c9154c44e7976be35a0790b217a28445c6c2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:813138f2f23c3f67c00cc3f899e890b4b46ad187b3c70730ab91bd63ff37fa6d`  
		Last Modified: Mon, 31 Mar 2025 17:41:30 GMT  
		Size: 5.8 MB (5776442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d132fb7bc19f6f368e535b5a46903e88d661e5c0f5e33c79b7d66b962039598`  
		Last Modified: Mon, 31 Mar 2025 20:44:23 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11` - unknown; unknown

```console
$ docker pull nats@sha256:13fe1989809a4185209660bba2e8a407b921e80a959889e94c8d6b18e6eadc66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cebd7eb7627ea55d24e6c1b36e5124796e00e1a2243414d5b3f65ff44089ec66`

```dockerfile
```

-	Layers:
	-	`sha256:a33f391d8364f479953478aa1b1ce3f8e6e05c31407e5d9ead5d4d5db6da559f`  
		Last Modified: Mon, 31 Mar 2025 20:44:29 GMT  
		Size: 10.7 KB (10708 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11` - linux; ppc64le

```console
$ docker pull nats@sha256:74e2df57ac704452ee531238216b3accd76025199ee310563732dd2c680227a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5757216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abd71cf45edbcaea354422b03a686d602fac79be9357fdbc6b5c05d8ab8309e5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:452917a8c6e0add88a19efed21ff3bf850d722622f476c3b9d4426f3dbaaffb7`  
		Last Modified: Mon, 31 Mar 2025 17:41:27 GMT  
		Size: 5.8 MB (5756706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc09a85b63b7a6867f196c8c27905ad711a7457fa91d3df80022bc3d24111b3`  
		Last Modified: Mon, 31 Mar 2025 20:07:44 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11` - unknown; unknown

```console
$ docker pull nats@sha256:9460476db24c3ccd45c6374ab5e0dfa8af2b95e6ed003b294fca69a3f6d49e72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8048c19445dcae5f87494cedbc4822265fb6848963d3958920bc8a77dc19881`

```dockerfile
```

-	Layers:
	-	`sha256:2e79f43f61fe3cbbfb9fa2ab55acbd3a3254d4378c81f4bef4392b1b18e91f10`  
		Last Modified: Mon, 31 Mar 2025 20:07:44 GMT  
		Size: 10.6 KB (10613 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11` - linux; s390x

```console
$ docker pull nats@sha256:6b9323c60c161cbd82daa5b02f46e55051f8540e7c9770dc1c2ed619086c6f53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6122555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb48b95165c0163d0de0d793f09fa9aaa8dbc79c4b50241ee9e33ac819b1a501`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:cdb5d3b73d4e5760c377e2d1a31f668fd95251ac45157f6a4c4d98139b337e23`  
		Last Modified: Mon, 31 Mar 2025 17:41:31 GMT  
		Size: 6.1 MB (6122046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16e9431fd0e418054b688573b0ef6c205ce09bcb9015c474b01a32d6800912d0`  
		Last Modified: Mon, 31 Mar 2025 20:07:36 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11` - unknown; unknown

```console
$ docker pull nats@sha256:2dfb1482f9d33c4a0f01a77e40b206f5b997b290b5e3899ee0c2678dd35731a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff58880fe981b8b31c473e8e992460d1ef7a218db9dd4ffc3a951750055bfd3`

```dockerfile
```

-	Layers:
	-	`sha256:9bb52fda18a732bf8f1ead6cd17dd200cfcae43fd84710a4ddb71372c0815f2b`  
		Last Modified: Mon, 31 Mar 2025 20:07:36 GMT  
		Size: 10.5 KB (10523 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11` - windows version 10.0.17763.7009; amd64

```console
$ docker pull nats@sha256:7523855e64c122a386122c97e7e122f78929c93ef1aaeabcfb818f96108eb526
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.4 MB (113369799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59c769ae1c19e869c3ab50a8bcc53b7a416139faa1f967bef29391891ff94a43`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 05 Mar 2025 21:54:26 GMT
RUN Apply image 10.0.17763.7009
# Mon, 31 Mar 2025 19:16:51 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Mon, 31 Mar 2025 19:16:54 GMT
RUN cmd /S /C #(nop) COPY file:cbd316e46d1e3baa5a0ffb6e227be5b521aa07a7cbe3a0513c0076ac28429bf3 in C:\nats-server.exe 
# Mon, 31 Mar 2025 19:16:55 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Mon, 31 Mar 2025 19:16:55 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Mon, 31 Mar 2025 19:16:56 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 31 Mar 2025 19:16:56 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:543388a101bf4d470af7e8817eff3f6f3b98f13d106939ab3f507a28f2825d0a`  
		Last Modified: Tue, 11 Mar 2025 22:40:48 GMT  
		Size: 106.9 MB (106907688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5764592bce5a260f59c0fc8af513aa702c03e73d61b9d9769cfb463cb5d345a4`  
		Last Modified: Mon, 31 Mar 2025 19:17:00 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c220ae7f5568ad8b19e77200fe2ab8b43bd7e66c8215b73f18cab048bf4c949b`  
		Last Modified: Mon, 31 Mar 2025 19:16:59 GMT  
		Size: 6.5 MB (6456094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24b9abd521fc3bf26173541357dca364e2aaa425fa95150aa12063ad86adbd0f`  
		Last Modified: Mon, 31 Mar 2025 19:16:59 GMT  
		Size: 1.7 KB (1684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47263123c2dca13a6ccd5e6c3f836df870102b1186585b3533a50841169f2d5d`  
		Last Modified: Mon, 31 Mar 2025 19:16:59 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb4c62df8bd6d5f27aca099be80d7290759022e9ed845409d9608b11f0e3db16`  
		Last Modified: Mon, 31 Mar 2025 19:16:58 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faf623903ff066d1e92e2c9250d8f7cd5a3230c1ea39d9cbe269fd63e735f4be`  
		Last Modified: Mon, 31 Mar 2025 19:16:59 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11-alpine`

```console
$ docker pull nats@sha256:222b8a7f2b9cbef1a51d412a5782ee75eac04062413d61c960b051e29c214115
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.11-alpine` - linux; amd64

```console
$ docker pull nats@sha256:d2bfc2b0b53f2a35c4b1c6fb432695b13dd232bdb551ea62c9fc00148520401f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10386128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6a871a4d4c93dc7e032ef72a3a722439e2ce32e96063585474891c6b654043f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
ENV NATS_SERVER=2.11.1-binary
# Mon, 31 Mar 2025 17:39:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='2499105f9e64bef55f168f634d34a586b710f6ac041639d8a18364f2b4f4c410' ;; 		armhf) natsArch='arm6'; sha256='31bc11906458e30c8028cdd0301de98713074db73f5e352f58ce4ecd6b1cc641' ;; 		armv7) natsArch='arm7'; sha256='432f4c47cf5adca05da67f1feaf969f6cea50ed9c3bb743a8bb76b8c5c583c8e' ;; 		x86_64) natsArch='amd64'; sha256='827497f99acd54eb0e4e8bfa3b0eb31dd51c6c259110de11a45a7fdacae6c5b3' ;; 		x86) natsArch='386'; sha256='651065e2170ee0f7e244425c0d0ba30a38776a7aef75e2d5cba0b8b11a950c54' ;; 		s390x) natsArch='s390x'; sha256='23e6ce6b70f9b973106d325eebb8bdd613040bedd4da980ff0aea2d2a7dc122e' ;; 		ppc64le) natsArch='ppc64le'; sha256='5341f41ef6298b05b72dd77c1ec055aeacb1b57dfd600ec888317347b3b4cbf8' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0643a146757fce88425f18db35388da5f1441b9e655395106fc3b6de8f7779a`  
		Last Modified: Mon, 31 Mar 2025 18:43:34 GMT  
		Size: 6.7 MB (6742912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f810863f848d47b0ec90164d81013c3f49b7d5d94bf9c42a73558dc7c46cfce`  
		Last Modified: Mon, 31 Mar 2025 18:43:33 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3295cd3199e071474b886bbbcf41ef4c12302ddbe5f1bd9283c8e119abcefe39`  
		Last Modified: Mon, 31 Mar 2025 18:43:33 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:7a817ee3d7045d87d4f49299e408201d1118ee221fdda63c5b66733871a32dea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89e54e9039e9d3c99605b12728bbecef9c9479593bdf67a68e894df9ecba60c4`

```dockerfile
```

-	Layers:
	-	`sha256:d380a2bbbdfb0718224f60b142dc29624483f0d28fa0552fb8e915ab9c1d69d2`  
		Last Modified: Mon, 31 Mar 2025 18:43:33 GMT  
		Size: 14.4 KB (14360 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:5b003eca587d5d1ded87d52f52a88b49c6091e2ae6ffcbcc9591ef31edfb1153
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9830711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd78fe0bc28317f1acadcd3ed9a09443a843f5cf68ef058de361ff0570543e01`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
ENV NATS_SERVER=2.11.1-binary
# Mon, 31 Mar 2025 17:39:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='2499105f9e64bef55f168f634d34a586b710f6ac041639d8a18364f2b4f4c410' ;; 		armhf) natsArch='arm6'; sha256='31bc11906458e30c8028cdd0301de98713074db73f5e352f58ce4ecd6b1cc641' ;; 		armv7) natsArch='arm7'; sha256='432f4c47cf5adca05da67f1feaf969f6cea50ed9c3bb743a8bb76b8c5c583c8e' ;; 		x86_64) natsArch='amd64'; sha256='827497f99acd54eb0e4e8bfa3b0eb31dd51c6c259110de11a45a7fdacae6c5b3' ;; 		x86) natsArch='386'; sha256='651065e2170ee0f7e244425c0d0ba30a38776a7aef75e2d5cba0b8b11a950c54' ;; 		s390x) natsArch='s390x'; sha256='23e6ce6b70f9b973106d325eebb8bdd613040bedd4da980ff0aea2d2a7dc122e' ;; 		ppc64le) natsArch='ppc64le'; sha256='5341f41ef6298b05b72dd77c1ec055aeacb1b57dfd600ec888317347b3b4cbf8' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c92f9bdc82b0d8955653988d31a42d2d808133d9b313a6f16c7c1fc6187ce7c3`  
		Last Modified: Mon, 31 Mar 2025 18:50:14 GMT  
		Size: 6.5 MB (6465008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f8f3e30080f28fb154a8574bfa9e68094196baa500cc70232b4b6a993d7d96`  
		Last Modified: Mon, 31 Mar 2025 18:50:13 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b07ed84ffecb4fe35014c6ec28f044236b811f87738a6e32d50061b6cdcf8913`  
		Last Modified: Mon, 31 Mar 2025 18:50:13 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:25ca21f30fda2b87f68ede801458791fdf7fb7571b1dfc4c5b92a80f7287b667
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fa2e55e1097547a0c5dc17d479d5b338734fce9c9e83240bf6a9eb19569188a`

```dockerfile
```

-	Layers:
	-	`sha256:f659982640e897f8f52e71b1b320e9ea56d5354063a38cf666928fe3ccf97400`  
		Last Modified: Mon, 31 Mar 2025 18:50:13 GMT  
		Size: 14.5 KB (14468 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:f6f902d9d220b13f8c52befb0e4f2520a530e999e9d0d7e3b4a7c96d1d6a2d4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9552225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f49a7e1e59161babacc6a62e07238abd7b349a8efc80a4bfd1523785ae8ece72`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
ENV NATS_SERVER=2.11.1-binary
# Mon, 31 Mar 2025 17:39:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='2499105f9e64bef55f168f634d34a586b710f6ac041639d8a18364f2b4f4c410' ;; 		armhf) natsArch='arm6'; sha256='31bc11906458e30c8028cdd0301de98713074db73f5e352f58ce4ecd6b1cc641' ;; 		armv7) natsArch='arm7'; sha256='432f4c47cf5adca05da67f1feaf969f6cea50ed9c3bb743a8bb76b8c5c583c8e' ;; 		x86_64) natsArch='amd64'; sha256='827497f99acd54eb0e4e8bfa3b0eb31dd51c6c259110de11a45a7fdacae6c5b3' ;; 		x86) natsArch='386'; sha256='651065e2170ee0f7e244425c0d0ba30a38776a7aef75e2d5cba0b8b11a950c54' ;; 		s390x) natsArch='s390x'; sha256='23e6ce6b70f9b973106d325eebb8bdd613040bedd4da980ff0aea2d2a7dc122e' ;; 		ppc64le) natsArch='ppc64le'; sha256='5341f41ef6298b05b72dd77c1ec055aeacb1b57dfd600ec888317347b3b4cbf8' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4be7f6d278a4174ef17dcd8c89848f067134976f430004cbed069643b89e46e8`  
		Last Modified: Mon, 31 Mar 2025 20:17:05 GMT  
		Size: 6.5 MB (6453133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825c724725f466486a81cdde1ec6a92840eb03f19fc7c9f6c2361d13f3398293`  
		Last Modified: Mon, 31 Mar 2025 20:17:04 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe87685444a72475e87e5ffbb1baff8c65017859e8e53c72573fc546273e8ef6`  
		Last Modified: Mon, 31 Mar 2025 20:17:04 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:860dd6d0c495dc91deb8a4c27e98247c01e7cc5ba0a4a80d0e33430aaa5695db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41756094504db64ff2b19360c941882401645db6e11cb7b116c9cc5d965c1002`

```dockerfile
```

-	Layers:
	-	`sha256:a83dd1e9193bcbd50a20cfab9ac07e63cb0d3f71b71000fc9b9e4456a63ddc2c`  
		Last Modified: Mon, 31 Mar 2025 20:17:04 GMT  
		Size: 14.5 KB (14468 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:90874ce66332c5ed35925509121cc1231be38266af7f5efe7097f37a54610dc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10234990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e934c9514dbf2966156ca2a5b60a8c62eab86a1d0e9316d96e587bc52837aff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
ENV NATS_SERVER=2.11.1-binary
# Mon, 31 Mar 2025 17:39:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='2499105f9e64bef55f168f634d34a586b710f6ac041639d8a18364f2b4f4c410' ;; 		armhf) natsArch='arm6'; sha256='31bc11906458e30c8028cdd0301de98713074db73f5e352f58ce4ecd6b1cc641' ;; 		armv7) natsArch='arm7'; sha256='432f4c47cf5adca05da67f1feaf969f6cea50ed9c3bb743a8bb76b8c5c583c8e' ;; 		x86_64) natsArch='amd64'; sha256='827497f99acd54eb0e4e8bfa3b0eb31dd51c6c259110de11a45a7fdacae6c5b3' ;; 		x86) natsArch='386'; sha256='651065e2170ee0f7e244425c0d0ba30a38776a7aef75e2d5cba0b8b11a950c54' ;; 		s390x) natsArch='s390x'; sha256='23e6ce6b70f9b973106d325eebb8bdd613040bedd4da980ff0aea2d2a7dc122e' ;; 		ppc64le) natsArch='ppc64le'; sha256='5341f41ef6298b05b72dd77c1ec055aeacb1b57dfd600ec888317347b3b4cbf8' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60797fdb0b4d910be869065ae81ab51200fbe5544785eb4efa8fc7cb9eb3033e`  
		Last Modified: Mon, 31 Mar 2025 20:11:13 GMT  
		Size: 6.2 MB (6240991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dda5bbcac3d56d1f2414331f89b9333ef3393083b91ce07a2face8802428335`  
		Last Modified: Mon, 31 Mar 2025 20:11:12 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c42e24e15c065a92a28be68d337a0e3f21fc9b4bee9e5e931179ab16a647031`  
		Last Modified: Mon, 31 Mar 2025 20:11:12 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:061fa681d240f27b08e83d14d855bff8191035c3944adf647afab28af9d67b5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a76bc64a67b68410441588e0e8ebc82c70ec9260099bfb6d4d5154152785d62`

```dockerfile
```

-	Layers:
	-	`sha256:5b3a7763692c9fffeebb31f53b8a14d7192250292c1661653d8912d27e67bd34`  
		Last Modified: Mon, 31 Mar 2025 20:11:12 GMT  
		Size: 14.5 KB (14512 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:f09b96d5bfacda0649814f91facba68b0ecca96de4ebdea7e17dfde79f1ada96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9796685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10c6bb2aed5161b870f53898cce57635999f3e6368d89209be712832cb7caae3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
ENV NATS_SERVER=2.11.1-binary
# Mon, 31 Mar 2025 17:39:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='2499105f9e64bef55f168f634d34a586b710f6ac041639d8a18364f2b4f4c410' ;; 		armhf) natsArch='arm6'; sha256='31bc11906458e30c8028cdd0301de98713074db73f5e352f58ce4ecd6b1cc641' ;; 		armv7) natsArch='arm7'; sha256='432f4c47cf5adca05da67f1feaf969f6cea50ed9c3bb743a8bb76b8c5c583c8e' ;; 		x86_64) natsArch='amd64'; sha256='827497f99acd54eb0e4e8bfa3b0eb31dd51c6c259110de11a45a7fdacae6c5b3' ;; 		x86) natsArch='386'; sha256='651065e2170ee0f7e244425c0d0ba30a38776a7aef75e2d5cba0b8b11a950c54' ;; 		s390x) natsArch='s390x'; sha256='23e6ce6b70f9b973106d325eebb8bdd613040bedd4da980ff0aea2d2a7dc122e' ;; 		ppc64le) natsArch='ppc64le'; sha256='5341f41ef6298b05b72dd77c1ec055aeacb1b57dfd600ec888317347b3b4cbf8' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:299c0ee564e4568e71d43a566874e9d853458071d554386ad5728913e55f5d42`  
		Last Modified: Mon, 31 Mar 2025 19:45:06 GMT  
		Size: 6.2 MB (6221370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1af98871a1453d715b201d0cb6c30c2e8240dd12ee7af67f4334bfb80877f3bb`  
		Last Modified: Mon, 31 Mar 2025 19:45:05 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:103d308786c4f17ef7f21746eadc69443e28518b33fd5534040a513bbb5acc64`  
		Last Modified: Mon, 31 Mar 2025 19:45:05 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:261ca6909da20cd9b36804c44211d5a257a4f0a8746e425a8d63cebe1ff274eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bf43f070134532bf9419111138ee6504a3b9010b90d59e6380375b5b9a4abcf`

```dockerfile
```

-	Layers:
	-	`sha256:09877c6dec89674d2ec4aefc8edd75ff573a4834ca2851e1a4be89994ffcd528`  
		Last Modified: Mon, 31 Mar 2025 19:45:05 GMT  
		Size: 14.4 KB (14427 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine` - linux; s390x

```console
$ docker pull nats@sha256:c14e89986785ed37ac2931d4b307ea84375f49180341e48c9024fe40f226decc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10053962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:893690471f61ea43e10126b7ceb4fd7a07fd98eb86fff95edc6cd8cf10d1e4ef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
ENV NATS_SERVER=2.11.1-binary
# Mon, 31 Mar 2025 17:39:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='2499105f9e64bef55f168f634d34a586b710f6ac041639d8a18364f2b4f4c410' ;; 		armhf) natsArch='arm6'; sha256='31bc11906458e30c8028cdd0301de98713074db73f5e352f58ce4ecd6b1cc641' ;; 		armv7) natsArch='arm7'; sha256='432f4c47cf5adca05da67f1feaf969f6cea50ed9c3bb743a8bb76b8c5c583c8e' ;; 		x86_64) natsArch='amd64'; sha256='827497f99acd54eb0e4e8bfa3b0eb31dd51c6c259110de11a45a7fdacae6c5b3' ;; 		x86) natsArch='386'; sha256='651065e2170ee0f7e244425c0d0ba30a38776a7aef75e2d5cba0b8b11a950c54' ;; 		s390x) natsArch='s390x'; sha256='23e6ce6b70f9b973106d325eebb8bdd613040bedd4da980ff0aea2d2a7dc122e' ;; 		ppc64le) natsArch='ppc64le'; sha256='5341f41ef6298b05b72dd77c1ec055aeacb1b57dfd600ec888317347b3b4cbf8' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67f000d40cf6813dabcb134d2a9b15f3b7eb5ba7dba583ad1df023b35efd9ca`  
		Last Modified: Mon, 31 Mar 2025 19:28:46 GMT  
		Size: 6.6 MB (6585424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4501a9ec92d7d9a89fd0e10cd2ba4c8fb93658a4d46301543d45d1f96b07ce32`  
		Last Modified: Mon, 31 Mar 2025 19:28:45 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06c2b65e72a2a266d2d783396559cd0ee8346a11e25f65ca2b21cc82de4174b6`  
		Last Modified: Mon, 31 Mar 2025 19:28:45 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:82ec15847478c49a8a561d7f21d2239bbea2614e277659456213e6bdd0f5dd49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:443d1aa445d5406aada9c0970885e837d983ea976af12760bad0de2704481f16`

```dockerfile
```

-	Layers:
	-	`sha256:688e4b2d5f0fdef107c3405864e3c9cc14ae13fd320ceddce8f4667dcde9d786`  
		Last Modified: Mon, 31 Mar 2025 19:28:45 GMT  
		Size: 14.4 KB (14360 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.11-alpine3.21`

```console
$ docker pull nats@sha256:222b8a7f2b9cbef1a51d412a5782ee75eac04062413d61c960b051e29c214115
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.11-alpine3.21` - linux; amd64

```console
$ docker pull nats@sha256:d2bfc2b0b53f2a35c4b1c6fb432695b13dd232bdb551ea62c9fc00148520401f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10386128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6a871a4d4c93dc7e032ef72a3a722439e2ce32e96063585474891c6b654043f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
ENV NATS_SERVER=2.11.1-binary
# Mon, 31 Mar 2025 17:39:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='2499105f9e64bef55f168f634d34a586b710f6ac041639d8a18364f2b4f4c410' ;; 		armhf) natsArch='arm6'; sha256='31bc11906458e30c8028cdd0301de98713074db73f5e352f58ce4ecd6b1cc641' ;; 		armv7) natsArch='arm7'; sha256='432f4c47cf5adca05da67f1feaf969f6cea50ed9c3bb743a8bb76b8c5c583c8e' ;; 		x86_64) natsArch='amd64'; sha256='827497f99acd54eb0e4e8bfa3b0eb31dd51c6c259110de11a45a7fdacae6c5b3' ;; 		x86) natsArch='386'; sha256='651065e2170ee0f7e244425c0d0ba30a38776a7aef75e2d5cba0b8b11a950c54' ;; 		s390x) natsArch='s390x'; sha256='23e6ce6b70f9b973106d325eebb8bdd613040bedd4da980ff0aea2d2a7dc122e' ;; 		ppc64le) natsArch='ppc64le'; sha256='5341f41ef6298b05b72dd77c1ec055aeacb1b57dfd600ec888317347b3b4cbf8' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0643a146757fce88425f18db35388da5f1441b9e655395106fc3b6de8f7779a`  
		Last Modified: Mon, 31 Mar 2025 18:43:34 GMT  
		Size: 6.7 MB (6742912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f810863f848d47b0ec90164d81013c3f49b7d5d94bf9c42a73558dc7c46cfce`  
		Last Modified: Mon, 31 Mar 2025 18:43:33 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3295cd3199e071474b886bbbcf41ef4c12302ddbe5f1bd9283c8e119abcefe39`  
		Last Modified: Mon, 31 Mar 2025 18:43:33 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:7a817ee3d7045d87d4f49299e408201d1118ee221fdda63c5b66733871a32dea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89e54e9039e9d3c99605b12728bbecef9c9479593bdf67a68e894df9ecba60c4`

```dockerfile
```

-	Layers:
	-	`sha256:d380a2bbbdfb0718224f60b142dc29624483f0d28fa0552fb8e915ab9c1d69d2`  
		Last Modified: Mon, 31 Mar 2025 18:43:33 GMT  
		Size: 14.4 KB (14360 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine3.21` - linux; arm variant v6

```console
$ docker pull nats@sha256:5b003eca587d5d1ded87d52f52a88b49c6091e2ae6ffcbcc9591ef31edfb1153
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9830711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd78fe0bc28317f1acadcd3ed9a09443a843f5cf68ef058de361ff0570543e01`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
ENV NATS_SERVER=2.11.1-binary
# Mon, 31 Mar 2025 17:39:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='2499105f9e64bef55f168f634d34a586b710f6ac041639d8a18364f2b4f4c410' ;; 		armhf) natsArch='arm6'; sha256='31bc11906458e30c8028cdd0301de98713074db73f5e352f58ce4ecd6b1cc641' ;; 		armv7) natsArch='arm7'; sha256='432f4c47cf5adca05da67f1feaf969f6cea50ed9c3bb743a8bb76b8c5c583c8e' ;; 		x86_64) natsArch='amd64'; sha256='827497f99acd54eb0e4e8bfa3b0eb31dd51c6c259110de11a45a7fdacae6c5b3' ;; 		x86) natsArch='386'; sha256='651065e2170ee0f7e244425c0d0ba30a38776a7aef75e2d5cba0b8b11a950c54' ;; 		s390x) natsArch='s390x'; sha256='23e6ce6b70f9b973106d325eebb8bdd613040bedd4da980ff0aea2d2a7dc122e' ;; 		ppc64le) natsArch='ppc64le'; sha256='5341f41ef6298b05b72dd77c1ec055aeacb1b57dfd600ec888317347b3b4cbf8' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c92f9bdc82b0d8955653988d31a42d2d808133d9b313a6f16c7c1fc6187ce7c3`  
		Last Modified: Mon, 31 Mar 2025 18:50:14 GMT  
		Size: 6.5 MB (6465008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f8f3e30080f28fb154a8574bfa9e68094196baa500cc70232b4b6a993d7d96`  
		Last Modified: Mon, 31 Mar 2025 18:50:13 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b07ed84ffecb4fe35014c6ec28f044236b811f87738a6e32d50061b6cdcf8913`  
		Last Modified: Mon, 31 Mar 2025 18:50:13 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:25ca21f30fda2b87f68ede801458791fdf7fb7571b1dfc4c5b92a80f7287b667
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fa2e55e1097547a0c5dc17d479d5b338734fce9c9e83240bf6a9eb19569188a`

```dockerfile
```

-	Layers:
	-	`sha256:f659982640e897f8f52e71b1b320e9ea56d5354063a38cf666928fe3ccf97400`  
		Last Modified: Mon, 31 Mar 2025 18:50:13 GMT  
		Size: 14.5 KB (14468 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine3.21` - linux; arm variant v7

```console
$ docker pull nats@sha256:f6f902d9d220b13f8c52befb0e4f2520a530e999e9d0d7e3b4a7c96d1d6a2d4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9552225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f49a7e1e59161babacc6a62e07238abd7b349a8efc80a4bfd1523785ae8ece72`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
ENV NATS_SERVER=2.11.1-binary
# Mon, 31 Mar 2025 17:39:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='2499105f9e64bef55f168f634d34a586b710f6ac041639d8a18364f2b4f4c410' ;; 		armhf) natsArch='arm6'; sha256='31bc11906458e30c8028cdd0301de98713074db73f5e352f58ce4ecd6b1cc641' ;; 		armv7) natsArch='arm7'; sha256='432f4c47cf5adca05da67f1feaf969f6cea50ed9c3bb743a8bb76b8c5c583c8e' ;; 		x86_64) natsArch='amd64'; sha256='827497f99acd54eb0e4e8bfa3b0eb31dd51c6c259110de11a45a7fdacae6c5b3' ;; 		x86) natsArch='386'; sha256='651065e2170ee0f7e244425c0d0ba30a38776a7aef75e2d5cba0b8b11a950c54' ;; 		s390x) natsArch='s390x'; sha256='23e6ce6b70f9b973106d325eebb8bdd613040bedd4da980ff0aea2d2a7dc122e' ;; 		ppc64le) natsArch='ppc64le'; sha256='5341f41ef6298b05b72dd77c1ec055aeacb1b57dfd600ec888317347b3b4cbf8' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4be7f6d278a4174ef17dcd8c89848f067134976f430004cbed069643b89e46e8`  
		Last Modified: Mon, 31 Mar 2025 20:17:05 GMT  
		Size: 6.5 MB (6453133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825c724725f466486a81cdde1ec6a92840eb03f19fc7c9f6c2361d13f3398293`  
		Last Modified: Mon, 31 Mar 2025 20:17:04 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe87685444a72475e87e5ffbb1baff8c65017859e8e53c72573fc546273e8ef6`  
		Last Modified: Mon, 31 Mar 2025 20:17:04 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:860dd6d0c495dc91deb8a4c27e98247c01e7cc5ba0a4a80d0e33430aaa5695db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41756094504db64ff2b19360c941882401645db6e11cb7b116c9cc5d965c1002`

```dockerfile
```

-	Layers:
	-	`sha256:a83dd1e9193bcbd50a20cfab9ac07e63cb0d3f71b71000fc9b9e4456a63ddc2c`  
		Last Modified: Mon, 31 Mar 2025 20:17:04 GMT  
		Size: 14.5 KB (14468 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:90874ce66332c5ed35925509121cc1231be38266af7f5efe7097f37a54610dc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10234990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e934c9514dbf2966156ca2a5b60a8c62eab86a1d0e9316d96e587bc52837aff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
ENV NATS_SERVER=2.11.1-binary
# Mon, 31 Mar 2025 17:39:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='2499105f9e64bef55f168f634d34a586b710f6ac041639d8a18364f2b4f4c410' ;; 		armhf) natsArch='arm6'; sha256='31bc11906458e30c8028cdd0301de98713074db73f5e352f58ce4ecd6b1cc641' ;; 		armv7) natsArch='arm7'; sha256='432f4c47cf5adca05da67f1feaf969f6cea50ed9c3bb743a8bb76b8c5c583c8e' ;; 		x86_64) natsArch='amd64'; sha256='827497f99acd54eb0e4e8bfa3b0eb31dd51c6c259110de11a45a7fdacae6c5b3' ;; 		x86) natsArch='386'; sha256='651065e2170ee0f7e244425c0d0ba30a38776a7aef75e2d5cba0b8b11a950c54' ;; 		s390x) natsArch='s390x'; sha256='23e6ce6b70f9b973106d325eebb8bdd613040bedd4da980ff0aea2d2a7dc122e' ;; 		ppc64le) natsArch='ppc64le'; sha256='5341f41ef6298b05b72dd77c1ec055aeacb1b57dfd600ec888317347b3b4cbf8' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60797fdb0b4d910be869065ae81ab51200fbe5544785eb4efa8fc7cb9eb3033e`  
		Last Modified: Mon, 31 Mar 2025 20:11:13 GMT  
		Size: 6.2 MB (6240991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dda5bbcac3d56d1f2414331f89b9333ef3393083b91ce07a2face8802428335`  
		Last Modified: Mon, 31 Mar 2025 20:11:12 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c42e24e15c065a92a28be68d337a0e3f21fc9b4bee9e5e931179ab16a647031`  
		Last Modified: Mon, 31 Mar 2025 20:11:12 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:061fa681d240f27b08e83d14d855bff8191035c3944adf647afab28af9d67b5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a76bc64a67b68410441588e0e8ebc82c70ec9260099bfb6d4d5154152785d62`

```dockerfile
```

-	Layers:
	-	`sha256:5b3a7763692c9fffeebb31f53b8a14d7192250292c1661653d8912d27e67bd34`  
		Last Modified: Mon, 31 Mar 2025 20:11:12 GMT  
		Size: 14.5 KB (14512 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine3.21` - linux; ppc64le

```console
$ docker pull nats@sha256:f09b96d5bfacda0649814f91facba68b0ecca96de4ebdea7e17dfde79f1ada96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9796685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10c6bb2aed5161b870f53898cce57635999f3e6368d89209be712832cb7caae3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
ENV NATS_SERVER=2.11.1-binary
# Mon, 31 Mar 2025 17:39:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='2499105f9e64bef55f168f634d34a586b710f6ac041639d8a18364f2b4f4c410' ;; 		armhf) natsArch='arm6'; sha256='31bc11906458e30c8028cdd0301de98713074db73f5e352f58ce4ecd6b1cc641' ;; 		armv7) natsArch='arm7'; sha256='432f4c47cf5adca05da67f1feaf969f6cea50ed9c3bb743a8bb76b8c5c583c8e' ;; 		x86_64) natsArch='amd64'; sha256='827497f99acd54eb0e4e8bfa3b0eb31dd51c6c259110de11a45a7fdacae6c5b3' ;; 		x86) natsArch='386'; sha256='651065e2170ee0f7e244425c0d0ba30a38776a7aef75e2d5cba0b8b11a950c54' ;; 		s390x) natsArch='s390x'; sha256='23e6ce6b70f9b973106d325eebb8bdd613040bedd4da980ff0aea2d2a7dc122e' ;; 		ppc64le) natsArch='ppc64le'; sha256='5341f41ef6298b05b72dd77c1ec055aeacb1b57dfd600ec888317347b3b4cbf8' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:299c0ee564e4568e71d43a566874e9d853458071d554386ad5728913e55f5d42`  
		Last Modified: Mon, 31 Mar 2025 19:45:06 GMT  
		Size: 6.2 MB (6221370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1af98871a1453d715b201d0cb6c30c2e8240dd12ee7af67f4334bfb80877f3bb`  
		Last Modified: Mon, 31 Mar 2025 19:45:05 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:103d308786c4f17ef7f21746eadc69443e28518b33fd5534040a513bbb5acc64`  
		Last Modified: Mon, 31 Mar 2025 19:45:05 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:261ca6909da20cd9b36804c44211d5a257a4f0a8746e425a8d63cebe1ff274eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bf43f070134532bf9419111138ee6504a3b9010b90d59e6380375b5b9a4abcf`

```dockerfile
```

-	Layers:
	-	`sha256:09877c6dec89674d2ec4aefc8edd75ff573a4834ca2851e1a4be89994ffcd528`  
		Last Modified: Mon, 31 Mar 2025 19:45:05 GMT  
		Size: 14.4 KB (14427 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine3.21` - linux; s390x

```console
$ docker pull nats@sha256:c14e89986785ed37ac2931d4b307ea84375f49180341e48c9024fe40f226decc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10053962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:893690471f61ea43e10126b7ceb4fd7a07fd98eb86fff95edc6cd8cf10d1e4ef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
ENV NATS_SERVER=2.11.1-binary
# Mon, 31 Mar 2025 17:39:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='2499105f9e64bef55f168f634d34a586b710f6ac041639d8a18364f2b4f4c410' ;; 		armhf) natsArch='arm6'; sha256='31bc11906458e30c8028cdd0301de98713074db73f5e352f58ce4ecd6b1cc641' ;; 		armv7) natsArch='arm7'; sha256='432f4c47cf5adca05da67f1feaf969f6cea50ed9c3bb743a8bb76b8c5c583c8e' ;; 		x86_64) natsArch='amd64'; sha256='827497f99acd54eb0e4e8bfa3b0eb31dd51c6c259110de11a45a7fdacae6c5b3' ;; 		x86) natsArch='386'; sha256='651065e2170ee0f7e244425c0d0ba30a38776a7aef75e2d5cba0b8b11a950c54' ;; 		s390x) natsArch='s390x'; sha256='23e6ce6b70f9b973106d325eebb8bdd613040bedd4da980ff0aea2d2a7dc122e' ;; 		ppc64le) natsArch='ppc64le'; sha256='5341f41ef6298b05b72dd77c1ec055aeacb1b57dfd600ec888317347b3b4cbf8' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67f000d40cf6813dabcb134d2a9b15f3b7eb5ba7dba583ad1df023b35efd9ca`  
		Last Modified: Mon, 31 Mar 2025 19:28:46 GMT  
		Size: 6.6 MB (6585424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4501a9ec92d7d9a89fd0e10cd2ba4c8fb93658a4d46301543d45d1f96b07ce32`  
		Last Modified: Mon, 31 Mar 2025 19:28:45 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06c2b65e72a2a266d2d783396559cd0ee8346a11e25f65ca2b21cc82de4174b6`  
		Last Modified: Mon, 31 Mar 2025 19:28:45 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:82ec15847478c49a8a561d7f21d2239bbea2614e277659456213e6bdd0f5dd49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:443d1aa445d5406aada9c0970885e837d983ea976af12760bad0de2704481f16`

```dockerfile
```

-	Layers:
	-	`sha256:688e4b2d5f0fdef107c3405864e3c9cc14ae13fd320ceddce8f4667dcde9d786`  
		Last Modified: Mon, 31 Mar 2025 19:28:45 GMT  
		Size: 14.4 KB (14360 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.11-linux`

```console
$ docker pull nats@sha256:c81104c29f774ab6ac6178391029a857ca1b201750c9ebefad70bee0b9162cf6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.11-linux` - linux; amd64

```console
$ docker pull nats@sha256:0b313c16824b8d98736c06153fa01af3c8d62eebc6298e9062fd2e00c0a3e865
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6282666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5a2333da61b6c9f0de1de8235aca52ee071283b0c8c6487d3ea15b4a0f9f8e2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:54120e60f5a574cbbfd83de2711330ae98499a27ff592bdb694994b87749dd23`  
		Last Modified: Mon, 31 Mar 2025 17:41:30 GMT  
		Size: 6.3 MB (6282155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71d71c31c70e45e814d8db85102321f1459be653c595cd91fafb76306cdf405e`  
		Last Modified: Mon, 31 Mar 2025 19:07:36 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-linux` - unknown; unknown

```console
$ docker pull nats@sha256:b8d62bc797363d5eab76aea96ec144d02b901da4dba8eb8bf31cc4e51e3a09d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbd51cd5b25ea5c4355cd2cde0e286d4f6da98802af9ed8b477001ff7ece4679`

```dockerfile
```

-	Layers:
	-	`sha256:19abc39a4cbb247bfa12363ce59bbce1e3bf861fddb9055c3a17e2d39d54d204`  
		Last Modified: Mon, 31 Mar 2025 19:07:36 GMT  
		Size: 10.5 KB (10523 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:af5758489c2981e0a1028dc47f82f0dd2d26e2fac7ac1e478a2a15a12029f6d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6002169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c17f13cf88d7cb6d029eafd34cd847cbacebb2131dc5b7ecfbed791e2958e6a4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:098bda892a4e7ddd77ca838f72ef9757e9b3cfae3c7bc97076a8dd0b6fd92597`  
		Last Modified: Mon, 31 Mar 2025 17:41:30 GMT  
		Size: 6.0 MB (6001660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff1d2651842734b21329c25e1004a4da19102e57001381e60bb4fd58723fe19`  
		Last Modified: Mon, 31 Mar 2025 19:07:08 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-linux` - unknown; unknown

```console
$ docker pull nats@sha256:736b8ee8472809de9731d9c426d2113e533e5ac68c9fbf4cd6bb44eb636b3d79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ffa52afcf9f827961f6f692daeb94f398721ac7559f559d56147558f6742150`

```dockerfile
```

-	Layers:
	-	`sha256:cc5887e8b88d73925b5364f9143ca37566f003a1560dffe173f7be8f10d66806`  
		Last Modified: Mon, 31 Mar 2025 19:07:08 GMT  
		Size: 10.7 KB (10650 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:f1752b6d8b3a5506fab1fdf93ce66a6bd6e934d33a3c230231458f254ff505a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5992492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68d3d700cbec0d68868397c08f331e9cee8a3e484035ab651de2414c1bc1039b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7ae07ef7aadc186e26516a3b1a5bacd27b42c41b8d63efc540622587ef29be07`  
		Last Modified: Mon, 31 Mar 2025 17:41:36 GMT  
		Size: 6.0 MB (5991983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d132fb7bc19f6f368e535b5a46903e88d661e5c0f5e33c79b7d66b962039598`  
		Last Modified: Mon, 31 Mar 2025 20:44:23 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-linux` - unknown; unknown

```console
$ docker pull nats@sha256:ff00ada993e928a0dbcd0e627e845b5f9c4d11042f0e089912b8ef2969c89876
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab26b373d46f30d56fc9b9ecf02d3c518eb5ab041a8fbb69e562b49b1a864d9d`

```dockerfile
```

-	Layers:
	-	`sha256:d552b4d64ce37965149a8aaeed3a0eebd251066efc77cb63ad2307f9d0bbdef7`  
		Last Modified: Mon, 31 Mar 2025 20:44:23 GMT  
		Size: 10.6 KB (10649 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a360fbbfeb6f19012e875675cf70ea15e5ea3d9e003d5ccf1a61adeed8d515c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5776951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aad8d86003a865c09c995830bd52c9154c44e7976be35a0790b217a28445c6c2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:813138f2f23c3f67c00cc3f899e890b4b46ad187b3c70730ab91bd63ff37fa6d`  
		Last Modified: Mon, 31 Mar 2025 17:41:30 GMT  
		Size: 5.8 MB (5776442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d132fb7bc19f6f368e535b5a46903e88d661e5c0f5e33c79b7d66b962039598`  
		Last Modified: Mon, 31 Mar 2025 20:44:23 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-linux` - unknown; unknown

```console
$ docker pull nats@sha256:13fe1989809a4185209660bba2e8a407b921e80a959889e94c8d6b18e6eadc66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cebd7eb7627ea55d24e6c1b36e5124796e00e1a2243414d5b3f65ff44089ec66`

```dockerfile
```

-	Layers:
	-	`sha256:a33f391d8364f479953478aa1b1ce3f8e6e05c31407e5d9ead5d4d5db6da559f`  
		Last Modified: Mon, 31 Mar 2025 20:44:29 GMT  
		Size: 10.7 KB (10708 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:74e2df57ac704452ee531238216b3accd76025199ee310563732dd2c680227a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5757216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abd71cf45edbcaea354422b03a686d602fac79be9357fdbc6b5c05d8ab8309e5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:452917a8c6e0add88a19efed21ff3bf850d722622f476c3b9d4426f3dbaaffb7`  
		Last Modified: Mon, 31 Mar 2025 17:41:27 GMT  
		Size: 5.8 MB (5756706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc09a85b63b7a6867f196c8c27905ad711a7457fa91d3df80022bc3d24111b3`  
		Last Modified: Mon, 31 Mar 2025 20:07:44 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-linux` - unknown; unknown

```console
$ docker pull nats@sha256:9460476db24c3ccd45c6374ab5e0dfa8af2b95e6ed003b294fca69a3f6d49e72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8048c19445dcae5f87494cedbc4822265fb6848963d3958920bc8a77dc19881`

```dockerfile
```

-	Layers:
	-	`sha256:2e79f43f61fe3cbbfb9fa2ab55acbd3a3254d4378c81f4bef4392b1b18e91f10`  
		Last Modified: Mon, 31 Mar 2025 20:07:44 GMT  
		Size: 10.6 KB (10613 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-linux` - linux; s390x

```console
$ docker pull nats@sha256:6b9323c60c161cbd82daa5b02f46e55051f8540e7c9770dc1c2ed619086c6f53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6122555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb48b95165c0163d0de0d793f09fa9aaa8dbc79c4b50241ee9e33ac819b1a501`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:cdb5d3b73d4e5760c377e2d1a31f668fd95251ac45157f6a4c4d98139b337e23`  
		Last Modified: Mon, 31 Mar 2025 17:41:31 GMT  
		Size: 6.1 MB (6122046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16e9431fd0e418054b688573b0ef6c205ce09bcb9015c474b01a32d6800912d0`  
		Last Modified: Mon, 31 Mar 2025 20:07:36 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-linux` - unknown; unknown

```console
$ docker pull nats@sha256:2dfb1482f9d33c4a0f01a77e40b206f5b997b290b5e3899ee0c2678dd35731a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff58880fe981b8b31c473e8e992460d1ef7a218db9dd4ffc3a951750055bfd3`

```dockerfile
```

-	Layers:
	-	`sha256:9bb52fda18a732bf8f1ead6cd17dd200cfcae43fd84710a4ddb71372c0815f2b`  
		Last Modified: Mon, 31 Mar 2025 20:07:36 GMT  
		Size: 10.5 KB (10523 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.11-nanoserver`

```console
$ docker pull nats@sha256:ab7919f36b0bf7f8b85e92aadeb04b95a0f3a5f1d2b33203d2ed60c8104ef5ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `nats:2.11-nanoserver` - windows version 10.0.17763.7009; amd64

```console
$ docker pull nats@sha256:7523855e64c122a386122c97e7e122f78929c93ef1aaeabcfb818f96108eb526
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.4 MB (113369799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59c769ae1c19e869c3ab50a8bcc53b7a416139faa1f967bef29391891ff94a43`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 05 Mar 2025 21:54:26 GMT
RUN Apply image 10.0.17763.7009
# Mon, 31 Mar 2025 19:16:51 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Mon, 31 Mar 2025 19:16:54 GMT
RUN cmd /S /C #(nop) COPY file:cbd316e46d1e3baa5a0ffb6e227be5b521aa07a7cbe3a0513c0076ac28429bf3 in C:\nats-server.exe 
# Mon, 31 Mar 2025 19:16:55 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Mon, 31 Mar 2025 19:16:55 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Mon, 31 Mar 2025 19:16:56 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 31 Mar 2025 19:16:56 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:543388a101bf4d470af7e8817eff3f6f3b98f13d106939ab3f507a28f2825d0a`  
		Last Modified: Tue, 11 Mar 2025 22:40:48 GMT  
		Size: 106.9 MB (106907688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5764592bce5a260f59c0fc8af513aa702c03e73d61b9d9769cfb463cb5d345a4`  
		Last Modified: Mon, 31 Mar 2025 19:17:00 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c220ae7f5568ad8b19e77200fe2ab8b43bd7e66c8215b73f18cab048bf4c949b`  
		Last Modified: Mon, 31 Mar 2025 19:16:59 GMT  
		Size: 6.5 MB (6456094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24b9abd521fc3bf26173541357dca364e2aaa425fa95150aa12063ad86adbd0f`  
		Last Modified: Mon, 31 Mar 2025 19:16:59 GMT  
		Size: 1.7 KB (1684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47263123c2dca13a6ccd5e6c3f836df870102b1186585b3533a50841169f2d5d`  
		Last Modified: Mon, 31 Mar 2025 19:16:59 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb4c62df8bd6d5f27aca099be80d7290759022e9ed845409d9608b11f0e3db16`  
		Last Modified: Mon, 31 Mar 2025 19:16:58 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faf623903ff066d1e92e2c9250d8f7cd5a3230c1ea39d9cbe269fd63e735f4be`  
		Last Modified: Mon, 31 Mar 2025 19:16:59 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11-nanoserver-1809`

```console
$ docker pull nats@sha256:ab7919f36b0bf7f8b85e92aadeb04b95a0f3a5f1d2b33203d2ed60c8104ef5ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `nats:2.11-nanoserver-1809` - windows version 10.0.17763.7009; amd64

```console
$ docker pull nats@sha256:7523855e64c122a386122c97e7e122f78929c93ef1aaeabcfb818f96108eb526
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.4 MB (113369799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59c769ae1c19e869c3ab50a8bcc53b7a416139faa1f967bef29391891ff94a43`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 05 Mar 2025 21:54:26 GMT
RUN Apply image 10.0.17763.7009
# Mon, 31 Mar 2025 19:16:51 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Mon, 31 Mar 2025 19:16:54 GMT
RUN cmd /S /C #(nop) COPY file:cbd316e46d1e3baa5a0ffb6e227be5b521aa07a7cbe3a0513c0076ac28429bf3 in C:\nats-server.exe 
# Mon, 31 Mar 2025 19:16:55 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Mon, 31 Mar 2025 19:16:55 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Mon, 31 Mar 2025 19:16:56 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 31 Mar 2025 19:16:56 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:543388a101bf4d470af7e8817eff3f6f3b98f13d106939ab3f507a28f2825d0a`  
		Last Modified: Tue, 11 Mar 2025 22:40:48 GMT  
		Size: 106.9 MB (106907688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5764592bce5a260f59c0fc8af513aa702c03e73d61b9d9769cfb463cb5d345a4`  
		Last Modified: Mon, 31 Mar 2025 19:17:00 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c220ae7f5568ad8b19e77200fe2ab8b43bd7e66c8215b73f18cab048bf4c949b`  
		Last Modified: Mon, 31 Mar 2025 19:16:59 GMT  
		Size: 6.5 MB (6456094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24b9abd521fc3bf26173541357dca364e2aaa425fa95150aa12063ad86adbd0f`  
		Last Modified: Mon, 31 Mar 2025 19:16:59 GMT  
		Size: 1.7 KB (1684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47263123c2dca13a6ccd5e6c3f836df870102b1186585b3533a50841169f2d5d`  
		Last Modified: Mon, 31 Mar 2025 19:16:59 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb4c62df8bd6d5f27aca099be80d7290759022e9ed845409d9608b11f0e3db16`  
		Last Modified: Mon, 31 Mar 2025 19:16:58 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faf623903ff066d1e92e2c9250d8f7cd5a3230c1ea39d9cbe269fd63e735f4be`  
		Last Modified: Mon, 31 Mar 2025 19:16:59 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11-scratch`

```console
$ docker pull nats@sha256:c81104c29f774ab6ac6178391029a857ca1b201750c9ebefad70bee0b9162cf6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.11-scratch` - linux; amd64

```console
$ docker pull nats@sha256:0b313c16824b8d98736c06153fa01af3c8d62eebc6298e9062fd2e00c0a3e865
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6282666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5a2333da61b6c9f0de1de8235aca52ee071283b0c8c6487d3ea15b4a0f9f8e2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:54120e60f5a574cbbfd83de2711330ae98499a27ff592bdb694994b87749dd23`  
		Last Modified: Mon, 31 Mar 2025 17:41:30 GMT  
		Size: 6.3 MB (6282155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71d71c31c70e45e814d8db85102321f1459be653c595cd91fafb76306cdf405e`  
		Last Modified: Mon, 31 Mar 2025 19:07:36 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:b8d62bc797363d5eab76aea96ec144d02b901da4dba8eb8bf31cc4e51e3a09d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbd51cd5b25ea5c4355cd2cde0e286d4f6da98802af9ed8b477001ff7ece4679`

```dockerfile
```

-	Layers:
	-	`sha256:19abc39a4cbb247bfa12363ce59bbce1e3bf861fddb9055c3a17e2d39d54d204`  
		Last Modified: Mon, 31 Mar 2025 19:07:36 GMT  
		Size: 10.5 KB (10523 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:af5758489c2981e0a1028dc47f82f0dd2d26e2fac7ac1e478a2a15a12029f6d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6002169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c17f13cf88d7cb6d029eafd34cd847cbacebb2131dc5b7ecfbed791e2958e6a4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:098bda892a4e7ddd77ca838f72ef9757e9b3cfae3c7bc97076a8dd0b6fd92597`  
		Last Modified: Mon, 31 Mar 2025 17:41:30 GMT  
		Size: 6.0 MB (6001660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff1d2651842734b21329c25e1004a4da19102e57001381e60bb4fd58723fe19`  
		Last Modified: Mon, 31 Mar 2025 19:07:08 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:736b8ee8472809de9731d9c426d2113e533e5ac68c9fbf4cd6bb44eb636b3d79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ffa52afcf9f827961f6f692daeb94f398721ac7559f559d56147558f6742150`

```dockerfile
```

-	Layers:
	-	`sha256:cc5887e8b88d73925b5364f9143ca37566f003a1560dffe173f7be8f10d66806`  
		Last Modified: Mon, 31 Mar 2025 19:07:08 GMT  
		Size: 10.7 KB (10650 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:f1752b6d8b3a5506fab1fdf93ce66a6bd6e934d33a3c230231458f254ff505a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5992492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68d3d700cbec0d68868397c08f331e9cee8a3e484035ab651de2414c1bc1039b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7ae07ef7aadc186e26516a3b1a5bacd27b42c41b8d63efc540622587ef29be07`  
		Last Modified: Mon, 31 Mar 2025 17:41:36 GMT  
		Size: 6.0 MB (5991983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d132fb7bc19f6f368e535b5a46903e88d661e5c0f5e33c79b7d66b962039598`  
		Last Modified: Mon, 31 Mar 2025 20:44:23 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:ff00ada993e928a0dbcd0e627e845b5f9c4d11042f0e089912b8ef2969c89876
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab26b373d46f30d56fc9b9ecf02d3c518eb5ab041a8fbb69e562b49b1a864d9d`

```dockerfile
```

-	Layers:
	-	`sha256:d552b4d64ce37965149a8aaeed3a0eebd251066efc77cb63ad2307f9d0bbdef7`  
		Last Modified: Mon, 31 Mar 2025 20:44:23 GMT  
		Size: 10.6 KB (10649 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a360fbbfeb6f19012e875675cf70ea15e5ea3d9e003d5ccf1a61adeed8d515c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5776951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aad8d86003a865c09c995830bd52c9154c44e7976be35a0790b217a28445c6c2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:813138f2f23c3f67c00cc3f899e890b4b46ad187b3c70730ab91bd63ff37fa6d`  
		Last Modified: Mon, 31 Mar 2025 17:41:30 GMT  
		Size: 5.8 MB (5776442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d132fb7bc19f6f368e535b5a46903e88d661e5c0f5e33c79b7d66b962039598`  
		Last Modified: Mon, 31 Mar 2025 20:44:23 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:13fe1989809a4185209660bba2e8a407b921e80a959889e94c8d6b18e6eadc66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cebd7eb7627ea55d24e6c1b36e5124796e00e1a2243414d5b3f65ff44089ec66`

```dockerfile
```

-	Layers:
	-	`sha256:a33f391d8364f479953478aa1b1ce3f8e6e05c31407e5d9ead5d4d5db6da559f`  
		Last Modified: Mon, 31 Mar 2025 20:44:29 GMT  
		Size: 10.7 KB (10708 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:74e2df57ac704452ee531238216b3accd76025199ee310563732dd2c680227a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5757216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abd71cf45edbcaea354422b03a686d602fac79be9357fdbc6b5c05d8ab8309e5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:452917a8c6e0add88a19efed21ff3bf850d722622f476c3b9d4426f3dbaaffb7`  
		Last Modified: Mon, 31 Mar 2025 17:41:27 GMT  
		Size: 5.8 MB (5756706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc09a85b63b7a6867f196c8c27905ad711a7457fa91d3df80022bc3d24111b3`  
		Last Modified: Mon, 31 Mar 2025 20:07:44 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:9460476db24c3ccd45c6374ab5e0dfa8af2b95e6ed003b294fca69a3f6d49e72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8048c19445dcae5f87494cedbc4822265fb6848963d3958920bc8a77dc19881`

```dockerfile
```

-	Layers:
	-	`sha256:2e79f43f61fe3cbbfb9fa2ab55acbd3a3254d4378c81f4bef4392b1b18e91f10`  
		Last Modified: Mon, 31 Mar 2025 20:07:44 GMT  
		Size: 10.6 KB (10613 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-scratch` - linux; s390x

```console
$ docker pull nats@sha256:6b9323c60c161cbd82daa5b02f46e55051f8540e7c9770dc1c2ed619086c6f53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6122555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb48b95165c0163d0de0d793f09fa9aaa8dbc79c4b50241ee9e33ac819b1a501`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:cdb5d3b73d4e5760c377e2d1a31f668fd95251ac45157f6a4c4d98139b337e23`  
		Last Modified: Mon, 31 Mar 2025 17:41:31 GMT  
		Size: 6.1 MB (6122046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16e9431fd0e418054b688573b0ef6c205ce09bcb9015c474b01a32d6800912d0`  
		Last Modified: Mon, 31 Mar 2025 20:07:36 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:2dfb1482f9d33c4a0f01a77e40b206f5b997b290b5e3899ee0c2678dd35731a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff58880fe981b8b31c473e8e992460d1ef7a218db9dd4ffc3a951750055bfd3`

```dockerfile
```

-	Layers:
	-	`sha256:9bb52fda18a732bf8f1ead6cd17dd200cfcae43fd84710a4ddb71372c0815f2b`  
		Last Modified: Mon, 31 Mar 2025 20:07:36 GMT  
		Size: 10.5 KB (10523 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.11-windowsservercore`

```console
$ docker pull nats@sha256:9d03bcf6cbd1a06b72b01b12931276f9f11d428800308790ac7d2c5e7f013153
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `nats:2.11-windowsservercore` - windows version 10.0.17763.7009; amd64

```console
$ docker pull nats@sha256:358cd0aed79a204ff4c8b5c055a03c487c5358d7455e0ffa579125eceef0d34e
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2158788658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ee73222ac79929936f4b58dc26a22b9521b1d61e7a78f7c5ed88a75f23f1374`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 05 Mar 2025 22:09:20 GMT
RUN Install update 10.0.17763.7009
# Mon, 31 Mar 2025 18:52:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 31 Mar 2025 18:52:57 GMT
ENV NATS_DOCKERIZED=1
# Mon, 31 Mar 2025 18:52:58 GMT
ENV NATS_SERVER=2.11.1-binary
# Mon, 31 Mar 2025 18:52:59 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.1-binary/nats-server-v2.11.1-binary-windows-amd64.zip
# Mon, 31 Mar 2025 18:52:59 GMT
ENV NATS_SERVER_SHASUM=2ab6b2c964fd5fe3b10a471cba309033f0756182f69228a65d1764197facf59c
# Mon, 31 Mar 2025 18:53:46 GMT
RUN Set-PSDebug -Trace 2
# Mon, 31 Mar 2025 18:54:06 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Mon, 31 Mar 2025 18:54:06 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Mon, 31 Mar 2025 18:54:07 GMT
EXPOSE 4222 6222 8222
# Mon, 31 Mar 2025 18:54:08 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 31 Mar 2025 18:54:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77bec5e4bac3c7f6dc5d56da5ffc11e72881485b3a55330c17c915ad653f955`  
		Last Modified: Tue, 11 Mar 2025 17:48:06 GMT  
		Size: 431.4 MB (431366277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35a6c48e83b6ecc670f12e09411b9f19d7fb0a878e1f86a6812563467340ff8`  
		Last Modified: Mon, 31 Mar 2025 18:54:13 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c158e67ae1fa853b1e146c6dd4e2b8f7e13aab94075904e788f4dfa3b8943322`  
		Last Modified: Mon, 31 Mar 2025 18:54:12 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6610f67e82d540d4cf11d12f87f1a68f8b42e4371905c52df1cade737e4f44c`  
		Last Modified: Mon, 31 Mar 2025 18:54:11 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0929886be3ca1628c185214c762369ea53c4afb47d0603d3d69fb4b471d01bf7`  
		Last Modified: Mon, 31 Mar 2025 18:54:12 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a89f7e18c6f6e8406fbe811630282ddd985e8899085b73506a0f39ac3c8fcf33`  
		Last Modified: Mon, 31 Mar 2025 18:54:11 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a904ed39f5ad31d12b93284fed611d377be64b1d3871e896c2e1c83415ff28`  
		Last Modified: Mon, 31 Mar 2025 18:54:11 GMT  
		Size: 333.8 KB (333807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5239d01ea32c2be9edfc2b25b142685efcbaedbadb1778166b52c0858df66464`  
		Last Modified: Mon, 31 Mar 2025 18:54:11 GMT  
		Size: 6.8 MB (6807873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56c6af05e936d2967cd915bd57f5faacef8b514317cd4de730f837f728d14487`  
		Last Modified: Mon, 31 Mar 2025 18:54:10 GMT  
		Size: 1.9 KB (1931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe56937824b786b5d064fe15be3435e14f26a022d00662003396c61194954e0`  
		Last Modified: Mon, 31 Mar 2025 18:54:10 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4aaffd9d1722fd09e9a67ad18073b6716178658c1f5517404d7b4180df3142f`  
		Last Modified: Mon, 31 Mar 2025 18:54:10 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdcbf0f98ff7504665d65ee0034ca94a89e45d2ecc47f808f87787d51427d265`  
		Last Modified: Mon, 31 Mar 2025 18:54:10 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11-windowsservercore-1809`

```console
$ docker pull nats@sha256:9d03bcf6cbd1a06b72b01b12931276f9f11d428800308790ac7d2c5e7f013153
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `nats:2.11-windowsservercore-1809` - windows version 10.0.17763.7009; amd64

```console
$ docker pull nats@sha256:358cd0aed79a204ff4c8b5c055a03c487c5358d7455e0ffa579125eceef0d34e
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2158788658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ee73222ac79929936f4b58dc26a22b9521b1d61e7a78f7c5ed88a75f23f1374`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 05 Mar 2025 22:09:20 GMT
RUN Install update 10.0.17763.7009
# Mon, 31 Mar 2025 18:52:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 31 Mar 2025 18:52:57 GMT
ENV NATS_DOCKERIZED=1
# Mon, 31 Mar 2025 18:52:58 GMT
ENV NATS_SERVER=2.11.1-binary
# Mon, 31 Mar 2025 18:52:59 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.1-binary/nats-server-v2.11.1-binary-windows-amd64.zip
# Mon, 31 Mar 2025 18:52:59 GMT
ENV NATS_SERVER_SHASUM=2ab6b2c964fd5fe3b10a471cba309033f0756182f69228a65d1764197facf59c
# Mon, 31 Mar 2025 18:53:46 GMT
RUN Set-PSDebug -Trace 2
# Mon, 31 Mar 2025 18:54:06 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Mon, 31 Mar 2025 18:54:06 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Mon, 31 Mar 2025 18:54:07 GMT
EXPOSE 4222 6222 8222
# Mon, 31 Mar 2025 18:54:08 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 31 Mar 2025 18:54:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77bec5e4bac3c7f6dc5d56da5ffc11e72881485b3a55330c17c915ad653f955`  
		Last Modified: Tue, 11 Mar 2025 17:48:06 GMT  
		Size: 431.4 MB (431366277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35a6c48e83b6ecc670f12e09411b9f19d7fb0a878e1f86a6812563467340ff8`  
		Last Modified: Mon, 31 Mar 2025 18:54:13 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c158e67ae1fa853b1e146c6dd4e2b8f7e13aab94075904e788f4dfa3b8943322`  
		Last Modified: Mon, 31 Mar 2025 18:54:12 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6610f67e82d540d4cf11d12f87f1a68f8b42e4371905c52df1cade737e4f44c`  
		Last Modified: Mon, 31 Mar 2025 18:54:11 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0929886be3ca1628c185214c762369ea53c4afb47d0603d3d69fb4b471d01bf7`  
		Last Modified: Mon, 31 Mar 2025 18:54:12 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a89f7e18c6f6e8406fbe811630282ddd985e8899085b73506a0f39ac3c8fcf33`  
		Last Modified: Mon, 31 Mar 2025 18:54:11 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a904ed39f5ad31d12b93284fed611d377be64b1d3871e896c2e1c83415ff28`  
		Last Modified: Mon, 31 Mar 2025 18:54:11 GMT  
		Size: 333.8 KB (333807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5239d01ea32c2be9edfc2b25b142685efcbaedbadb1778166b52c0858df66464`  
		Last Modified: Mon, 31 Mar 2025 18:54:11 GMT  
		Size: 6.8 MB (6807873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56c6af05e936d2967cd915bd57f5faacef8b514317cd4de730f837f728d14487`  
		Last Modified: Mon, 31 Mar 2025 18:54:10 GMT  
		Size: 1.9 KB (1931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe56937824b786b5d064fe15be3435e14f26a022d00662003396c61194954e0`  
		Last Modified: Mon, 31 Mar 2025 18:54:10 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4aaffd9d1722fd09e9a67ad18073b6716178658c1f5517404d7b4180df3142f`  
		Last Modified: Mon, 31 Mar 2025 18:54:10 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdcbf0f98ff7504665d65ee0034ca94a89e45d2ecc47f808f87787d51427d265`  
		Last Modified: Mon, 31 Mar 2025 18:54:10 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11.1-binary`

```console
$ docker pull nats@sha256:76fe53997736051e3511ddc26d585abd679fe3a30dbf74d19418bb0035fde031
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 13
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown
	-	windows version 10.0.17763.7009; amd64

### `nats:2.11.1-binary` - linux; amd64

```console
$ docker pull nats@sha256:0b313c16824b8d98736c06153fa01af3c8d62eebc6298e9062fd2e00c0a3e865
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6282666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5a2333da61b6c9f0de1de8235aca52ee071283b0c8c6487d3ea15b4a0f9f8e2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:54120e60f5a574cbbfd83de2711330ae98499a27ff592bdb694994b87749dd23`  
		Last Modified: Mon, 31 Mar 2025 17:41:30 GMT  
		Size: 6.3 MB (6282155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71d71c31c70e45e814d8db85102321f1459be653c595cd91fafb76306cdf405e`  
		Last Modified: Mon, 31 Mar 2025 19:07:36 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.1-binary` - unknown; unknown

```console
$ docker pull nats@sha256:b8d62bc797363d5eab76aea96ec144d02b901da4dba8eb8bf31cc4e51e3a09d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbd51cd5b25ea5c4355cd2cde0e286d4f6da98802af9ed8b477001ff7ece4679`

```dockerfile
```

-	Layers:
	-	`sha256:19abc39a4cbb247bfa12363ce59bbce1e3bf861fddb9055c3a17e2d39d54d204`  
		Last Modified: Mon, 31 Mar 2025 19:07:36 GMT  
		Size: 10.5 KB (10523 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.1-binary` - linux; arm variant v6

```console
$ docker pull nats@sha256:af5758489c2981e0a1028dc47f82f0dd2d26e2fac7ac1e478a2a15a12029f6d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6002169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c17f13cf88d7cb6d029eafd34cd847cbacebb2131dc5b7ecfbed791e2958e6a4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:098bda892a4e7ddd77ca838f72ef9757e9b3cfae3c7bc97076a8dd0b6fd92597`  
		Last Modified: Mon, 31 Mar 2025 17:41:30 GMT  
		Size: 6.0 MB (6001660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff1d2651842734b21329c25e1004a4da19102e57001381e60bb4fd58723fe19`  
		Last Modified: Mon, 31 Mar 2025 19:07:08 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.1-binary` - unknown; unknown

```console
$ docker pull nats@sha256:736b8ee8472809de9731d9c426d2113e533e5ac68c9fbf4cd6bb44eb636b3d79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ffa52afcf9f827961f6f692daeb94f398721ac7559f559d56147558f6742150`

```dockerfile
```

-	Layers:
	-	`sha256:cc5887e8b88d73925b5364f9143ca37566f003a1560dffe173f7be8f10d66806`  
		Last Modified: Mon, 31 Mar 2025 19:07:08 GMT  
		Size: 10.7 KB (10650 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.1-binary` - linux; arm variant v7

```console
$ docker pull nats@sha256:f1752b6d8b3a5506fab1fdf93ce66a6bd6e934d33a3c230231458f254ff505a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5992492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68d3d700cbec0d68868397c08f331e9cee8a3e484035ab651de2414c1bc1039b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7ae07ef7aadc186e26516a3b1a5bacd27b42c41b8d63efc540622587ef29be07`  
		Last Modified: Mon, 31 Mar 2025 17:41:36 GMT  
		Size: 6.0 MB (5991983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d132fb7bc19f6f368e535b5a46903e88d661e5c0f5e33c79b7d66b962039598`  
		Last Modified: Mon, 31 Mar 2025 20:44:23 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.1-binary` - unknown; unknown

```console
$ docker pull nats@sha256:ff00ada993e928a0dbcd0e627e845b5f9c4d11042f0e089912b8ef2969c89876
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab26b373d46f30d56fc9b9ecf02d3c518eb5ab041a8fbb69e562b49b1a864d9d`

```dockerfile
```

-	Layers:
	-	`sha256:d552b4d64ce37965149a8aaeed3a0eebd251066efc77cb63ad2307f9d0bbdef7`  
		Last Modified: Mon, 31 Mar 2025 20:44:23 GMT  
		Size: 10.6 KB (10649 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.1-binary` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a360fbbfeb6f19012e875675cf70ea15e5ea3d9e003d5ccf1a61adeed8d515c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5776951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aad8d86003a865c09c995830bd52c9154c44e7976be35a0790b217a28445c6c2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:813138f2f23c3f67c00cc3f899e890b4b46ad187b3c70730ab91bd63ff37fa6d`  
		Last Modified: Mon, 31 Mar 2025 17:41:30 GMT  
		Size: 5.8 MB (5776442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d132fb7bc19f6f368e535b5a46903e88d661e5c0f5e33c79b7d66b962039598`  
		Last Modified: Mon, 31 Mar 2025 20:44:23 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.1-binary` - unknown; unknown

```console
$ docker pull nats@sha256:13fe1989809a4185209660bba2e8a407b921e80a959889e94c8d6b18e6eadc66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cebd7eb7627ea55d24e6c1b36e5124796e00e1a2243414d5b3f65ff44089ec66`

```dockerfile
```

-	Layers:
	-	`sha256:a33f391d8364f479953478aa1b1ce3f8e6e05c31407e5d9ead5d4d5db6da559f`  
		Last Modified: Mon, 31 Mar 2025 20:44:29 GMT  
		Size: 10.7 KB (10708 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.1-binary` - linux; ppc64le

```console
$ docker pull nats@sha256:74e2df57ac704452ee531238216b3accd76025199ee310563732dd2c680227a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5757216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abd71cf45edbcaea354422b03a686d602fac79be9357fdbc6b5c05d8ab8309e5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:452917a8c6e0add88a19efed21ff3bf850d722622f476c3b9d4426f3dbaaffb7`  
		Last Modified: Mon, 31 Mar 2025 17:41:27 GMT  
		Size: 5.8 MB (5756706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc09a85b63b7a6867f196c8c27905ad711a7457fa91d3df80022bc3d24111b3`  
		Last Modified: Mon, 31 Mar 2025 20:07:44 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.1-binary` - unknown; unknown

```console
$ docker pull nats@sha256:9460476db24c3ccd45c6374ab5e0dfa8af2b95e6ed003b294fca69a3f6d49e72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8048c19445dcae5f87494cedbc4822265fb6848963d3958920bc8a77dc19881`

```dockerfile
```

-	Layers:
	-	`sha256:2e79f43f61fe3cbbfb9fa2ab55acbd3a3254d4378c81f4bef4392b1b18e91f10`  
		Last Modified: Mon, 31 Mar 2025 20:07:44 GMT  
		Size: 10.6 KB (10613 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.1-binary` - linux; s390x

```console
$ docker pull nats@sha256:6b9323c60c161cbd82daa5b02f46e55051f8540e7c9770dc1c2ed619086c6f53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6122555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb48b95165c0163d0de0d793f09fa9aaa8dbc79c4b50241ee9e33ac819b1a501`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:cdb5d3b73d4e5760c377e2d1a31f668fd95251ac45157f6a4c4d98139b337e23`  
		Last Modified: Mon, 31 Mar 2025 17:41:31 GMT  
		Size: 6.1 MB (6122046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16e9431fd0e418054b688573b0ef6c205ce09bcb9015c474b01a32d6800912d0`  
		Last Modified: Mon, 31 Mar 2025 20:07:36 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.1-binary` - unknown; unknown

```console
$ docker pull nats@sha256:2dfb1482f9d33c4a0f01a77e40b206f5b997b290b5e3899ee0c2678dd35731a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff58880fe981b8b31c473e8e992460d1ef7a218db9dd4ffc3a951750055bfd3`

```dockerfile
```

-	Layers:
	-	`sha256:9bb52fda18a732bf8f1ead6cd17dd200cfcae43fd84710a4ddb71372c0815f2b`  
		Last Modified: Mon, 31 Mar 2025 20:07:36 GMT  
		Size: 10.5 KB (10523 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.1-binary` - windows version 10.0.17763.7009; amd64

```console
$ docker pull nats@sha256:7523855e64c122a386122c97e7e122f78929c93ef1aaeabcfb818f96108eb526
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.4 MB (113369799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59c769ae1c19e869c3ab50a8bcc53b7a416139faa1f967bef29391891ff94a43`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 05 Mar 2025 21:54:26 GMT
RUN Apply image 10.0.17763.7009
# Mon, 31 Mar 2025 19:16:51 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Mon, 31 Mar 2025 19:16:54 GMT
RUN cmd /S /C #(nop) COPY file:cbd316e46d1e3baa5a0ffb6e227be5b521aa07a7cbe3a0513c0076ac28429bf3 in C:\nats-server.exe 
# Mon, 31 Mar 2025 19:16:55 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Mon, 31 Mar 2025 19:16:55 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Mon, 31 Mar 2025 19:16:56 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 31 Mar 2025 19:16:56 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:543388a101bf4d470af7e8817eff3f6f3b98f13d106939ab3f507a28f2825d0a`  
		Last Modified: Tue, 11 Mar 2025 22:40:48 GMT  
		Size: 106.9 MB (106907688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5764592bce5a260f59c0fc8af513aa702c03e73d61b9d9769cfb463cb5d345a4`  
		Last Modified: Mon, 31 Mar 2025 19:17:00 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c220ae7f5568ad8b19e77200fe2ab8b43bd7e66c8215b73f18cab048bf4c949b`  
		Last Modified: Mon, 31 Mar 2025 19:16:59 GMT  
		Size: 6.5 MB (6456094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24b9abd521fc3bf26173541357dca364e2aaa425fa95150aa12063ad86adbd0f`  
		Last Modified: Mon, 31 Mar 2025 19:16:59 GMT  
		Size: 1.7 KB (1684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47263123c2dca13a6ccd5e6c3f836df870102b1186585b3533a50841169f2d5d`  
		Last Modified: Mon, 31 Mar 2025 19:16:59 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb4c62df8bd6d5f27aca099be80d7290759022e9ed845409d9608b11f0e3db16`  
		Last Modified: Mon, 31 Mar 2025 19:16:58 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faf623903ff066d1e92e2c9250d8f7cd5a3230c1ea39d9cbe269fd63e735f4be`  
		Last Modified: Mon, 31 Mar 2025 19:16:59 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11.1-binary-alpine`

```console
$ docker pull nats@sha256:222b8a7f2b9cbef1a51d412a5782ee75eac04062413d61c960b051e29c214115
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.11.1-binary-alpine` - linux; amd64

```console
$ docker pull nats@sha256:d2bfc2b0b53f2a35c4b1c6fb432695b13dd232bdb551ea62c9fc00148520401f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10386128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6a871a4d4c93dc7e032ef72a3a722439e2ce32e96063585474891c6b654043f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
ENV NATS_SERVER=2.11.1-binary
# Mon, 31 Mar 2025 17:39:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='2499105f9e64bef55f168f634d34a586b710f6ac041639d8a18364f2b4f4c410' ;; 		armhf) natsArch='arm6'; sha256='31bc11906458e30c8028cdd0301de98713074db73f5e352f58ce4ecd6b1cc641' ;; 		armv7) natsArch='arm7'; sha256='432f4c47cf5adca05da67f1feaf969f6cea50ed9c3bb743a8bb76b8c5c583c8e' ;; 		x86_64) natsArch='amd64'; sha256='827497f99acd54eb0e4e8bfa3b0eb31dd51c6c259110de11a45a7fdacae6c5b3' ;; 		x86) natsArch='386'; sha256='651065e2170ee0f7e244425c0d0ba30a38776a7aef75e2d5cba0b8b11a950c54' ;; 		s390x) natsArch='s390x'; sha256='23e6ce6b70f9b973106d325eebb8bdd613040bedd4da980ff0aea2d2a7dc122e' ;; 		ppc64le) natsArch='ppc64le'; sha256='5341f41ef6298b05b72dd77c1ec055aeacb1b57dfd600ec888317347b3b4cbf8' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0643a146757fce88425f18db35388da5f1441b9e655395106fc3b6de8f7779a`  
		Last Modified: Mon, 31 Mar 2025 18:43:34 GMT  
		Size: 6.7 MB (6742912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f810863f848d47b0ec90164d81013c3f49b7d5d94bf9c42a73558dc7c46cfce`  
		Last Modified: Mon, 31 Mar 2025 18:43:33 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3295cd3199e071474b886bbbcf41ef4c12302ddbe5f1bd9283c8e119abcefe39`  
		Last Modified: Mon, 31 Mar 2025 18:43:33 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.1-binary-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:7a817ee3d7045d87d4f49299e408201d1118ee221fdda63c5b66733871a32dea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89e54e9039e9d3c99605b12728bbecef9c9479593bdf67a68e894df9ecba60c4`

```dockerfile
```

-	Layers:
	-	`sha256:d380a2bbbdfb0718224f60b142dc29624483f0d28fa0552fb8e915ab9c1d69d2`  
		Last Modified: Mon, 31 Mar 2025 18:43:33 GMT  
		Size: 14.4 KB (14360 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.1-binary-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:5b003eca587d5d1ded87d52f52a88b49c6091e2ae6ffcbcc9591ef31edfb1153
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9830711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd78fe0bc28317f1acadcd3ed9a09443a843f5cf68ef058de361ff0570543e01`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
ENV NATS_SERVER=2.11.1-binary
# Mon, 31 Mar 2025 17:39:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='2499105f9e64bef55f168f634d34a586b710f6ac041639d8a18364f2b4f4c410' ;; 		armhf) natsArch='arm6'; sha256='31bc11906458e30c8028cdd0301de98713074db73f5e352f58ce4ecd6b1cc641' ;; 		armv7) natsArch='arm7'; sha256='432f4c47cf5adca05da67f1feaf969f6cea50ed9c3bb743a8bb76b8c5c583c8e' ;; 		x86_64) natsArch='amd64'; sha256='827497f99acd54eb0e4e8bfa3b0eb31dd51c6c259110de11a45a7fdacae6c5b3' ;; 		x86) natsArch='386'; sha256='651065e2170ee0f7e244425c0d0ba30a38776a7aef75e2d5cba0b8b11a950c54' ;; 		s390x) natsArch='s390x'; sha256='23e6ce6b70f9b973106d325eebb8bdd613040bedd4da980ff0aea2d2a7dc122e' ;; 		ppc64le) natsArch='ppc64le'; sha256='5341f41ef6298b05b72dd77c1ec055aeacb1b57dfd600ec888317347b3b4cbf8' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c92f9bdc82b0d8955653988d31a42d2d808133d9b313a6f16c7c1fc6187ce7c3`  
		Last Modified: Mon, 31 Mar 2025 18:50:14 GMT  
		Size: 6.5 MB (6465008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f8f3e30080f28fb154a8574bfa9e68094196baa500cc70232b4b6a993d7d96`  
		Last Modified: Mon, 31 Mar 2025 18:50:13 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b07ed84ffecb4fe35014c6ec28f044236b811f87738a6e32d50061b6cdcf8913`  
		Last Modified: Mon, 31 Mar 2025 18:50:13 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.1-binary-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:25ca21f30fda2b87f68ede801458791fdf7fb7571b1dfc4c5b92a80f7287b667
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fa2e55e1097547a0c5dc17d479d5b338734fce9c9e83240bf6a9eb19569188a`

```dockerfile
```

-	Layers:
	-	`sha256:f659982640e897f8f52e71b1b320e9ea56d5354063a38cf666928fe3ccf97400`  
		Last Modified: Mon, 31 Mar 2025 18:50:13 GMT  
		Size: 14.5 KB (14468 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.1-binary-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:f6f902d9d220b13f8c52befb0e4f2520a530e999e9d0d7e3b4a7c96d1d6a2d4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9552225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f49a7e1e59161babacc6a62e07238abd7b349a8efc80a4bfd1523785ae8ece72`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
ENV NATS_SERVER=2.11.1-binary
# Mon, 31 Mar 2025 17:39:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='2499105f9e64bef55f168f634d34a586b710f6ac041639d8a18364f2b4f4c410' ;; 		armhf) natsArch='arm6'; sha256='31bc11906458e30c8028cdd0301de98713074db73f5e352f58ce4ecd6b1cc641' ;; 		armv7) natsArch='arm7'; sha256='432f4c47cf5adca05da67f1feaf969f6cea50ed9c3bb743a8bb76b8c5c583c8e' ;; 		x86_64) natsArch='amd64'; sha256='827497f99acd54eb0e4e8bfa3b0eb31dd51c6c259110de11a45a7fdacae6c5b3' ;; 		x86) natsArch='386'; sha256='651065e2170ee0f7e244425c0d0ba30a38776a7aef75e2d5cba0b8b11a950c54' ;; 		s390x) natsArch='s390x'; sha256='23e6ce6b70f9b973106d325eebb8bdd613040bedd4da980ff0aea2d2a7dc122e' ;; 		ppc64le) natsArch='ppc64le'; sha256='5341f41ef6298b05b72dd77c1ec055aeacb1b57dfd600ec888317347b3b4cbf8' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4be7f6d278a4174ef17dcd8c89848f067134976f430004cbed069643b89e46e8`  
		Last Modified: Mon, 31 Mar 2025 20:17:05 GMT  
		Size: 6.5 MB (6453133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825c724725f466486a81cdde1ec6a92840eb03f19fc7c9f6c2361d13f3398293`  
		Last Modified: Mon, 31 Mar 2025 20:17:04 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe87685444a72475e87e5ffbb1baff8c65017859e8e53c72573fc546273e8ef6`  
		Last Modified: Mon, 31 Mar 2025 20:17:04 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.1-binary-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:860dd6d0c495dc91deb8a4c27e98247c01e7cc5ba0a4a80d0e33430aaa5695db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41756094504db64ff2b19360c941882401645db6e11cb7b116c9cc5d965c1002`

```dockerfile
```

-	Layers:
	-	`sha256:a83dd1e9193bcbd50a20cfab9ac07e63cb0d3f71b71000fc9b9e4456a63ddc2c`  
		Last Modified: Mon, 31 Mar 2025 20:17:04 GMT  
		Size: 14.5 KB (14468 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.1-binary-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:90874ce66332c5ed35925509121cc1231be38266af7f5efe7097f37a54610dc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10234990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e934c9514dbf2966156ca2a5b60a8c62eab86a1d0e9316d96e587bc52837aff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
ENV NATS_SERVER=2.11.1-binary
# Mon, 31 Mar 2025 17:39:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='2499105f9e64bef55f168f634d34a586b710f6ac041639d8a18364f2b4f4c410' ;; 		armhf) natsArch='arm6'; sha256='31bc11906458e30c8028cdd0301de98713074db73f5e352f58ce4ecd6b1cc641' ;; 		armv7) natsArch='arm7'; sha256='432f4c47cf5adca05da67f1feaf969f6cea50ed9c3bb743a8bb76b8c5c583c8e' ;; 		x86_64) natsArch='amd64'; sha256='827497f99acd54eb0e4e8bfa3b0eb31dd51c6c259110de11a45a7fdacae6c5b3' ;; 		x86) natsArch='386'; sha256='651065e2170ee0f7e244425c0d0ba30a38776a7aef75e2d5cba0b8b11a950c54' ;; 		s390x) natsArch='s390x'; sha256='23e6ce6b70f9b973106d325eebb8bdd613040bedd4da980ff0aea2d2a7dc122e' ;; 		ppc64le) natsArch='ppc64le'; sha256='5341f41ef6298b05b72dd77c1ec055aeacb1b57dfd600ec888317347b3b4cbf8' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60797fdb0b4d910be869065ae81ab51200fbe5544785eb4efa8fc7cb9eb3033e`  
		Last Modified: Mon, 31 Mar 2025 20:11:13 GMT  
		Size: 6.2 MB (6240991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dda5bbcac3d56d1f2414331f89b9333ef3393083b91ce07a2face8802428335`  
		Last Modified: Mon, 31 Mar 2025 20:11:12 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c42e24e15c065a92a28be68d337a0e3f21fc9b4bee9e5e931179ab16a647031`  
		Last Modified: Mon, 31 Mar 2025 20:11:12 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.1-binary-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:061fa681d240f27b08e83d14d855bff8191035c3944adf647afab28af9d67b5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a76bc64a67b68410441588e0e8ebc82c70ec9260099bfb6d4d5154152785d62`

```dockerfile
```

-	Layers:
	-	`sha256:5b3a7763692c9fffeebb31f53b8a14d7192250292c1661653d8912d27e67bd34`  
		Last Modified: Mon, 31 Mar 2025 20:11:12 GMT  
		Size: 14.5 KB (14512 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.1-binary-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:f09b96d5bfacda0649814f91facba68b0ecca96de4ebdea7e17dfde79f1ada96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9796685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10c6bb2aed5161b870f53898cce57635999f3e6368d89209be712832cb7caae3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
ENV NATS_SERVER=2.11.1-binary
# Mon, 31 Mar 2025 17:39:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='2499105f9e64bef55f168f634d34a586b710f6ac041639d8a18364f2b4f4c410' ;; 		armhf) natsArch='arm6'; sha256='31bc11906458e30c8028cdd0301de98713074db73f5e352f58ce4ecd6b1cc641' ;; 		armv7) natsArch='arm7'; sha256='432f4c47cf5adca05da67f1feaf969f6cea50ed9c3bb743a8bb76b8c5c583c8e' ;; 		x86_64) natsArch='amd64'; sha256='827497f99acd54eb0e4e8bfa3b0eb31dd51c6c259110de11a45a7fdacae6c5b3' ;; 		x86) natsArch='386'; sha256='651065e2170ee0f7e244425c0d0ba30a38776a7aef75e2d5cba0b8b11a950c54' ;; 		s390x) natsArch='s390x'; sha256='23e6ce6b70f9b973106d325eebb8bdd613040bedd4da980ff0aea2d2a7dc122e' ;; 		ppc64le) natsArch='ppc64le'; sha256='5341f41ef6298b05b72dd77c1ec055aeacb1b57dfd600ec888317347b3b4cbf8' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:299c0ee564e4568e71d43a566874e9d853458071d554386ad5728913e55f5d42`  
		Last Modified: Mon, 31 Mar 2025 19:45:06 GMT  
		Size: 6.2 MB (6221370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1af98871a1453d715b201d0cb6c30c2e8240dd12ee7af67f4334bfb80877f3bb`  
		Last Modified: Mon, 31 Mar 2025 19:45:05 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:103d308786c4f17ef7f21746eadc69443e28518b33fd5534040a513bbb5acc64`  
		Last Modified: Mon, 31 Mar 2025 19:45:05 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.1-binary-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:261ca6909da20cd9b36804c44211d5a257a4f0a8746e425a8d63cebe1ff274eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bf43f070134532bf9419111138ee6504a3b9010b90d59e6380375b5b9a4abcf`

```dockerfile
```

-	Layers:
	-	`sha256:09877c6dec89674d2ec4aefc8edd75ff573a4834ca2851e1a4be89994ffcd528`  
		Last Modified: Mon, 31 Mar 2025 19:45:05 GMT  
		Size: 14.4 KB (14427 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.1-binary-alpine` - linux; s390x

```console
$ docker pull nats@sha256:c14e89986785ed37ac2931d4b307ea84375f49180341e48c9024fe40f226decc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10053962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:893690471f61ea43e10126b7ceb4fd7a07fd98eb86fff95edc6cd8cf10d1e4ef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
ENV NATS_SERVER=2.11.1-binary
# Mon, 31 Mar 2025 17:39:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='2499105f9e64bef55f168f634d34a586b710f6ac041639d8a18364f2b4f4c410' ;; 		armhf) natsArch='arm6'; sha256='31bc11906458e30c8028cdd0301de98713074db73f5e352f58ce4ecd6b1cc641' ;; 		armv7) natsArch='arm7'; sha256='432f4c47cf5adca05da67f1feaf969f6cea50ed9c3bb743a8bb76b8c5c583c8e' ;; 		x86_64) natsArch='amd64'; sha256='827497f99acd54eb0e4e8bfa3b0eb31dd51c6c259110de11a45a7fdacae6c5b3' ;; 		x86) natsArch='386'; sha256='651065e2170ee0f7e244425c0d0ba30a38776a7aef75e2d5cba0b8b11a950c54' ;; 		s390x) natsArch='s390x'; sha256='23e6ce6b70f9b973106d325eebb8bdd613040bedd4da980ff0aea2d2a7dc122e' ;; 		ppc64le) natsArch='ppc64le'; sha256='5341f41ef6298b05b72dd77c1ec055aeacb1b57dfd600ec888317347b3b4cbf8' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67f000d40cf6813dabcb134d2a9b15f3b7eb5ba7dba583ad1df023b35efd9ca`  
		Last Modified: Mon, 31 Mar 2025 19:28:46 GMT  
		Size: 6.6 MB (6585424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4501a9ec92d7d9a89fd0e10cd2ba4c8fb93658a4d46301543d45d1f96b07ce32`  
		Last Modified: Mon, 31 Mar 2025 19:28:45 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06c2b65e72a2a266d2d783396559cd0ee8346a11e25f65ca2b21cc82de4174b6`  
		Last Modified: Mon, 31 Mar 2025 19:28:45 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.1-binary-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:82ec15847478c49a8a561d7f21d2239bbea2614e277659456213e6bdd0f5dd49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:443d1aa445d5406aada9c0970885e837d983ea976af12760bad0de2704481f16`

```dockerfile
```

-	Layers:
	-	`sha256:688e4b2d5f0fdef107c3405864e3c9cc14ae13fd320ceddce8f4667dcde9d786`  
		Last Modified: Mon, 31 Mar 2025 19:28:45 GMT  
		Size: 14.4 KB (14360 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.11.1-binary-alpine3.21`

```console
$ docker pull nats@sha256:222b8a7f2b9cbef1a51d412a5782ee75eac04062413d61c960b051e29c214115
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.11.1-binary-alpine3.21` - linux; amd64

```console
$ docker pull nats@sha256:d2bfc2b0b53f2a35c4b1c6fb432695b13dd232bdb551ea62c9fc00148520401f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10386128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6a871a4d4c93dc7e032ef72a3a722439e2ce32e96063585474891c6b654043f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
ENV NATS_SERVER=2.11.1-binary
# Mon, 31 Mar 2025 17:39:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='2499105f9e64bef55f168f634d34a586b710f6ac041639d8a18364f2b4f4c410' ;; 		armhf) natsArch='arm6'; sha256='31bc11906458e30c8028cdd0301de98713074db73f5e352f58ce4ecd6b1cc641' ;; 		armv7) natsArch='arm7'; sha256='432f4c47cf5adca05da67f1feaf969f6cea50ed9c3bb743a8bb76b8c5c583c8e' ;; 		x86_64) natsArch='amd64'; sha256='827497f99acd54eb0e4e8bfa3b0eb31dd51c6c259110de11a45a7fdacae6c5b3' ;; 		x86) natsArch='386'; sha256='651065e2170ee0f7e244425c0d0ba30a38776a7aef75e2d5cba0b8b11a950c54' ;; 		s390x) natsArch='s390x'; sha256='23e6ce6b70f9b973106d325eebb8bdd613040bedd4da980ff0aea2d2a7dc122e' ;; 		ppc64le) natsArch='ppc64le'; sha256='5341f41ef6298b05b72dd77c1ec055aeacb1b57dfd600ec888317347b3b4cbf8' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0643a146757fce88425f18db35388da5f1441b9e655395106fc3b6de8f7779a`  
		Last Modified: Mon, 31 Mar 2025 18:43:34 GMT  
		Size: 6.7 MB (6742912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f810863f848d47b0ec90164d81013c3f49b7d5d94bf9c42a73558dc7c46cfce`  
		Last Modified: Mon, 31 Mar 2025 18:43:33 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3295cd3199e071474b886bbbcf41ef4c12302ddbe5f1bd9283c8e119abcefe39`  
		Last Modified: Mon, 31 Mar 2025 18:43:33 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.1-binary-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:7a817ee3d7045d87d4f49299e408201d1118ee221fdda63c5b66733871a32dea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89e54e9039e9d3c99605b12728bbecef9c9479593bdf67a68e894df9ecba60c4`

```dockerfile
```

-	Layers:
	-	`sha256:d380a2bbbdfb0718224f60b142dc29624483f0d28fa0552fb8e915ab9c1d69d2`  
		Last Modified: Mon, 31 Mar 2025 18:43:33 GMT  
		Size: 14.4 KB (14360 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.1-binary-alpine3.21` - linux; arm variant v6

```console
$ docker pull nats@sha256:5b003eca587d5d1ded87d52f52a88b49c6091e2ae6ffcbcc9591ef31edfb1153
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9830711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd78fe0bc28317f1acadcd3ed9a09443a843f5cf68ef058de361ff0570543e01`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
ENV NATS_SERVER=2.11.1-binary
# Mon, 31 Mar 2025 17:39:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='2499105f9e64bef55f168f634d34a586b710f6ac041639d8a18364f2b4f4c410' ;; 		armhf) natsArch='arm6'; sha256='31bc11906458e30c8028cdd0301de98713074db73f5e352f58ce4ecd6b1cc641' ;; 		armv7) natsArch='arm7'; sha256='432f4c47cf5adca05da67f1feaf969f6cea50ed9c3bb743a8bb76b8c5c583c8e' ;; 		x86_64) natsArch='amd64'; sha256='827497f99acd54eb0e4e8bfa3b0eb31dd51c6c259110de11a45a7fdacae6c5b3' ;; 		x86) natsArch='386'; sha256='651065e2170ee0f7e244425c0d0ba30a38776a7aef75e2d5cba0b8b11a950c54' ;; 		s390x) natsArch='s390x'; sha256='23e6ce6b70f9b973106d325eebb8bdd613040bedd4da980ff0aea2d2a7dc122e' ;; 		ppc64le) natsArch='ppc64le'; sha256='5341f41ef6298b05b72dd77c1ec055aeacb1b57dfd600ec888317347b3b4cbf8' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c92f9bdc82b0d8955653988d31a42d2d808133d9b313a6f16c7c1fc6187ce7c3`  
		Last Modified: Mon, 31 Mar 2025 18:50:14 GMT  
		Size: 6.5 MB (6465008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f8f3e30080f28fb154a8574bfa9e68094196baa500cc70232b4b6a993d7d96`  
		Last Modified: Mon, 31 Mar 2025 18:50:13 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b07ed84ffecb4fe35014c6ec28f044236b811f87738a6e32d50061b6cdcf8913`  
		Last Modified: Mon, 31 Mar 2025 18:50:13 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.1-binary-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:25ca21f30fda2b87f68ede801458791fdf7fb7571b1dfc4c5b92a80f7287b667
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fa2e55e1097547a0c5dc17d479d5b338734fce9c9e83240bf6a9eb19569188a`

```dockerfile
```

-	Layers:
	-	`sha256:f659982640e897f8f52e71b1b320e9ea56d5354063a38cf666928fe3ccf97400`  
		Last Modified: Mon, 31 Mar 2025 18:50:13 GMT  
		Size: 14.5 KB (14468 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.1-binary-alpine3.21` - linux; arm variant v7

```console
$ docker pull nats@sha256:f6f902d9d220b13f8c52befb0e4f2520a530e999e9d0d7e3b4a7c96d1d6a2d4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9552225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f49a7e1e59161babacc6a62e07238abd7b349a8efc80a4bfd1523785ae8ece72`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
ENV NATS_SERVER=2.11.1-binary
# Mon, 31 Mar 2025 17:39:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='2499105f9e64bef55f168f634d34a586b710f6ac041639d8a18364f2b4f4c410' ;; 		armhf) natsArch='arm6'; sha256='31bc11906458e30c8028cdd0301de98713074db73f5e352f58ce4ecd6b1cc641' ;; 		armv7) natsArch='arm7'; sha256='432f4c47cf5adca05da67f1feaf969f6cea50ed9c3bb743a8bb76b8c5c583c8e' ;; 		x86_64) natsArch='amd64'; sha256='827497f99acd54eb0e4e8bfa3b0eb31dd51c6c259110de11a45a7fdacae6c5b3' ;; 		x86) natsArch='386'; sha256='651065e2170ee0f7e244425c0d0ba30a38776a7aef75e2d5cba0b8b11a950c54' ;; 		s390x) natsArch='s390x'; sha256='23e6ce6b70f9b973106d325eebb8bdd613040bedd4da980ff0aea2d2a7dc122e' ;; 		ppc64le) natsArch='ppc64le'; sha256='5341f41ef6298b05b72dd77c1ec055aeacb1b57dfd600ec888317347b3b4cbf8' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4be7f6d278a4174ef17dcd8c89848f067134976f430004cbed069643b89e46e8`  
		Last Modified: Mon, 31 Mar 2025 20:17:05 GMT  
		Size: 6.5 MB (6453133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825c724725f466486a81cdde1ec6a92840eb03f19fc7c9f6c2361d13f3398293`  
		Last Modified: Mon, 31 Mar 2025 20:17:04 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe87685444a72475e87e5ffbb1baff8c65017859e8e53c72573fc546273e8ef6`  
		Last Modified: Mon, 31 Mar 2025 20:17:04 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.1-binary-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:860dd6d0c495dc91deb8a4c27e98247c01e7cc5ba0a4a80d0e33430aaa5695db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41756094504db64ff2b19360c941882401645db6e11cb7b116c9cc5d965c1002`

```dockerfile
```

-	Layers:
	-	`sha256:a83dd1e9193bcbd50a20cfab9ac07e63cb0d3f71b71000fc9b9e4456a63ddc2c`  
		Last Modified: Mon, 31 Mar 2025 20:17:04 GMT  
		Size: 14.5 KB (14468 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.1-binary-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:90874ce66332c5ed35925509121cc1231be38266af7f5efe7097f37a54610dc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10234990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e934c9514dbf2966156ca2a5b60a8c62eab86a1d0e9316d96e587bc52837aff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
ENV NATS_SERVER=2.11.1-binary
# Mon, 31 Mar 2025 17:39:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='2499105f9e64bef55f168f634d34a586b710f6ac041639d8a18364f2b4f4c410' ;; 		armhf) natsArch='arm6'; sha256='31bc11906458e30c8028cdd0301de98713074db73f5e352f58ce4ecd6b1cc641' ;; 		armv7) natsArch='arm7'; sha256='432f4c47cf5adca05da67f1feaf969f6cea50ed9c3bb743a8bb76b8c5c583c8e' ;; 		x86_64) natsArch='amd64'; sha256='827497f99acd54eb0e4e8bfa3b0eb31dd51c6c259110de11a45a7fdacae6c5b3' ;; 		x86) natsArch='386'; sha256='651065e2170ee0f7e244425c0d0ba30a38776a7aef75e2d5cba0b8b11a950c54' ;; 		s390x) natsArch='s390x'; sha256='23e6ce6b70f9b973106d325eebb8bdd613040bedd4da980ff0aea2d2a7dc122e' ;; 		ppc64le) natsArch='ppc64le'; sha256='5341f41ef6298b05b72dd77c1ec055aeacb1b57dfd600ec888317347b3b4cbf8' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60797fdb0b4d910be869065ae81ab51200fbe5544785eb4efa8fc7cb9eb3033e`  
		Last Modified: Mon, 31 Mar 2025 20:11:13 GMT  
		Size: 6.2 MB (6240991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dda5bbcac3d56d1f2414331f89b9333ef3393083b91ce07a2face8802428335`  
		Last Modified: Mon, 31 Mar 2025 20:11:12 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c42e24e15c065a92a28be68d337a0e3f21fc9b4bee9e5e931179ab16a647031`  
		Last Modified: Mon, 31 Mar 2025 20:11:12 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.1-binary-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:061fa681d240f27b08e83d14d855bff8191035c3944adf647afab28af9d67b5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a76bc64a67b68410441588e0e8ebc82c70ec9260099bfb6d4d5154152785d62`

```dockerfile
```

-	Layers:
	-	`sha256:5b3a7763692c9fffeebb31f53b8a14d7192250292c1661653d8912d27e67bd34`  
		Last Modified: Mon, 31 Mar 2025 20:11:12 GMT  
		Size: 14.5 KB (14512 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.1-binary-alpine3.21` - linux; ppc64le

```console
$ docker pull nats@sha256:f09b96d5bfacda0649814f91facba68b0ecca96de4ebdea7e17dfde79f1ada96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9796685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10c6bb2aed5161b870f53898cce57635999f3e6368d89209be712832cb7caae3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
ENV NATS_SERVER=2.11.1-binary
# Mon, 31 Mar 2025 17:39:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='2499105f9e64bef55f168f634d34a586b710f6ac041639d8a18364f2b4f4c410' ;; 		armhf) natsArch='arm6'; sha256='31bc11906458e30c8028cdd0301de98713074db73f5e352f58ce4ecd6b1cc641' ;; 		armv7) natsArch='arm7'; sha256='432f4c47cf5adca05da67f1feaf969f6cea50ed9c3bb743a8bb76b8c5c583c8e' ;; 		x86_64) natsArch='amd64'; sha256='827497f99acd54eb0e4e8bfa3b0eb31dd51c6c259110de11a45a7fdacae6c5b3' ;; 		x86) natsArch='386'; sha256='651065e2170ee0f7e244425c0d0ba30a38776a7aef75e2d5cba0b8b11a950c54' ;; 		s390x) natsArch='s390x'; sha256='23e6ce6b70f9b973106d325eebb8bdd613040bedd4da980ff0aea2d2a7dc122e' ;; 		ppc64le) natsArch='ppc64le'; sha256='5341f41ef6298b05b72dd77c1ec055aeacb1b57dfd600ec888317347b3b4cbf8' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:299c0ee564e4568e71d43a566874e9d853458071d554386ad5728913e55f5d42`  
		Last Modified: Mon, 31 Mar 2025 19:45:06 GMT  
		Size: 6.2 MB (6221370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1af98871a1453d715b201d0cb6c30c2e8240dd12ee7af67f4334bfb80877f3bb`  
		Last Modified: Mon, 31 Mar 2025 19:45:05 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:103d308786c4f17ef7f21746eadc69443e28518b33fd5534040a513bbb5acc64`  
		Last Modified: Mon, 31 Mar 2025 19:45:05 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.1-binary-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:261ca6909da20cd9b36804c44211d5a257a4f0a8746e425a8d63cebe1ff274eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bf43f070134532bf9419111138ee6504a3b9010b90d59e6380375b5b9a4abcf`

```dockerfile
```

-	Layers:
	-	`sha256:09877c6dec89674d2ec4aefc8edd75ff573a4834ca2851e1a4be89994ffcd528`  
		Last Modified: Mon, 31 Mar 2025 19:45:05 GMT  
		Size: 14.4 KB (14427 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.1-binary-alpine3.21` - linux; s390x

```console
$ docker pull nats@sha256:c14e89986785ed37ac2931d4b307ea84375f49180341e48c9024fe40f226decc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10053962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:893690471f61ea43e10126b7ceb4fd7a07fd98eb86fff95edc6cd8cf10d1e4ef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
ENV NATS_SERVER=2.11.1-binary
# Mon, 31 Mar 2025 17:39:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='2499105f9e64bef55f168f634d34a586b710f6ac041639d8a18364f2b4f4c410' ;; 		armhf) natsArch='arm6'; sha256='31bc11906458e30c8028cdd0301de98713074db73f5e352f58ce4ecd6b1cc641' ;; 		armv7) natsArch='arm7'; sha256='432f4c47cf5adca05da67f1feaf969f6cea50ed9c3bb743a8bb76b8c5c583c8e' ;; 		x86_64) natsArch='amd64'; sha256='827497f99acd54eb0e4e8bfa3b0eb31dd51c6c259110de11a45a7fdacae6c5b3' ;; 		x86) natsArch='386'; sha256='651065e2170ee0f7e244425c0d0ba30a38776a7aef75e2d5cba0b8b11a950c54' ;; 		s390x) natsArch='s390x'; sha256='23e6ce6b70f9b973106d325eebb8bdd613040bedd4da980ff0aea2d2a7dc122e' ;; 		ppc64le) natsArch='ppc64le'; sha256='5341f41ef6298b05b72dd77c1ec055aeacb1b57dfd600ec888317347b3b4cbf8' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67f000d40cf6813dabcb134d2a9b15f3b7eb5ba7dba583ad1df023b35efd9ca`  
		Last Modified: Mon, 31 Mar 2025 19:28:46 GMT  
		Size: 6.6 MB (6585424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4501a9ec92d7d9a89fd0e10cd2ba4c8fb93658a4d46301543d45d1f96b07ce32`  
		Last Modified: Mon, 31 Mar 2025 19:28:45 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06c2b65e72a2a266d2d783396559cd0ee8346a11e25f65ca2b21cc82de4174b6`  
		Last Modified: Mon, 31 Mar 2025 19:28:45 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.1-binary-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:82ec15847478c49a8a561d7f21d2239bbea2614e277659456213e6bdd0f5dd49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:443d1aa445d5406aada9c0970885e837d983ea976af12760bad0de2704481f16`

```dockerfile
```

-	Layers:
	-	`sha256:688e4b2d5f0fdef107c3405864e3c9cc14ae13fd320ceddce8f4667dcde9d786`  
		Last Modified: Mon, 31 Mar 2025 19:28:45 GMT  
		Size: 14.4 KB (14360 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.11.1-binary-linux`

```console
$ docker pull nats@sha256:c81104c29f774ab6ac6178391029a857ca1b201750c9ebefad70bee0b9162cf6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.11.1-binary-linux` - linux; amd64

```console
$ docker pull nats@sha256:0b313c16824b8d98736c06153fa01af3c8d62eebc6298e9062fd2e00c0a3e865
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6282666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5a2333da61b6c9f0de1de8235aca52ee071283b0c8c6487d3ea15b4a0f9f8e2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:54120e60f5a574cbbfd83de2711330ae98499a27ff592bdb694994b87749dd23`  
		Last Modified: Mon, 31 Mar 2025 17:41:30 GMT  
		Size: 6.3 MB (6282155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71d71c31c70e45e814d8db85102321f1459be653c595cd91fafb76306cdf405e`  
		Last Modified: Mon, 31 Mar 2025 19:07:36 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.1-binary-linux` - unknown; unknown

```console
$ docker pull nats@sha256:b8d62bc797363d5eab76aea96ec144d02b901da4dba8eb8bf31cc4e51e3a09d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbd51cd5b25ea5c4355cd2cde0e286d4f6da98802af9ed8b477001ff7ece4679`

```dockerfile
```

-	Layers:
	-	`sha256:19abc39a4cbb247bfa12363ce59bbce1e3bf861fddb9055c3a17e2d39d54d204`  
		Last Modified: Mon, 31 Mar 2025 19:07:36 GMT  
		Size: 10.5 KB (10523 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.1-binary-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:af5758489c2981e0a1028dc47f82f0dd2d26e2fac7ac1e478a2a15a12029f6d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6002169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c17f13cf88d7cb6d029eafd34cd847cbacebb2131dc5b7ecfbed791e2958e6a4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:098bda892a4e7ddd77ca838f72ef9757e9b3cfae3c7bc97076a8dd0b6fd92597`  
		Last Modified: Mon, 31 Mar 2025 17:41:30 GMT  
		Size: 6.0 MB (6001660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff1d2651842734b21329c25e1004a4da19102e57001381e60bb4fd58723fe19`  
		Last Modified: Mon, 31 Mar 2025 19:07:08 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.1-binary-linux` - unknown; unknown

```console
$ docker pull nats@sha256:736b8ee8472809de9731d9c426d2113e533e5ac68c9fbf4cd6bb44eb636b3d79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ffa52afcf9f827961f6f692daeb94f398721ac7559f559d56147558f6742150`

```dockerfile
```

-	Layers:
	-	`sha256:cc5887e8b88d73925b5364f9143ca37566f003a1560dffe173f7be8f10d66806`  
		Last Modified: Mon, 31 Mar 2025 19:07:08 GMT  
		Size: 10.7 KB (10650 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.1-binary-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:f1752b6d8b3a5506fab1fdf93ce66a6bd6e934d33a3c230231458f254ff505a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5992492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68d3d700cbec0d68868397c08f331e9cee8a3e484035ab651de2414c1bc1039b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7ae07ef7aadc186e26516a3b1a5bacd27b42c41b8d63efc540622587ef29be07`  
		Last Modified: Mon, 31 Mar 2025 17:41:36 GMT  
		Size: 6.0 MB (5991983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d132fb7bc19f6f368e535b5a46903e88d661e5c0f5e33c79b7d66b962039598`  
		Last Modified: Mon, 31 Mar 2025 20:44:23 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.1-binary-linux` - unknown; unknown

```console
$ docker pull nats@sha256:ff00ada993e928a0dbcd0e627e845b5f9c4d11042f0e089912b8ef2969c89876
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab26b373d46f30d56fc9b9ecf02d3c518eb5ab041a8fbb69e562b49b1a864d9d`

```dockerfile
```

-	Layers:
	-	`sha256:d552b4d64ce37965149a8aaeed3a0eebd251066efc77cb63ad2307f9d0bbdef7`  
		Last Modified: Mon, 31 Mar 2025 20:44:23 GMT  
		Size: 10.6 KB (10649 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.1-binary-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a360fbbfeb6f19012e875675cf70ea15e5ea3d9e003d5ccf1a61adeed8d515c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5776951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aad8d86003a865c09c995830bd52c9154c44e7976be35a0790b217a28445c6c2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:813138f2f23c3f67c00cc3f899e890b4b46ad187b3c70730ab91bd63ff37fa6d`  
		Last Modified: Mon, 31 Mar 2025 17:41:30 GMT  
		Size: 5.8 MB (5776442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d132fb7bc19f6f368e535b5a46903e88d661e5c0f5e33c79b7d66b962039598`  
		Last Modified: Mon, 31 Mar 2025 20:44:23 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.1-binary-linux` - unknown; unknown

```console
$ docker pull nats@sha256:13fe1989809a4185209660bba2e8a407b921e80a959889e94c8d6b18e6eadc66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cebd7eb7627ea55d24e6c1b36e5124796e00e1a2243414d5b3f65ff44089ec66`

```dockerfile
```

-	Layers:
	-	`sha256:a33f391d8364f479953478aa1b1ce3f8e6e05c31407e5d9ead5d4d5db6da559f`  
		Last Modified: Mon, 31 Mar 2025 20:44:29 GMT  
		Size: 10.7 KB (10708 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.1-binary-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:74e2df57ac704452ee531238216b3accd76025199ee310563732dd2c680227a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5757216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abd71cf45edbcaea354422b03a686d602fac79be9357fdbc6b5c05d8ab8309e5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:452917a8c6e0add88a19efed21ff3bf850d722622f476c3b9d4426f3dbaaffb7`  
		Last Modified: Mon, 31 Mar 2025 17:41:27 GMT  
		Size: 5.8 MB (5756706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc09a85b63b7a6867f196c8c27905ad711a7457fa91d3df80022bc3d24111b3`  
		Last Modified: Mon, 31 Mar 2025 20:07:44 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.1-binary-linux` - unknown; unknown

```console
$ docker pull nats@sha256:9460476db24c3ccd45c6374ab5e0dfa8af2b95e6ed003b294fca69a3f6d49e72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8048c19445dcae5f87494cedbc4822265fb6848963d3958920bc8a77dc19881`

```dockerfile
```

-	Layers:
	-	`sha256:2e79f43f61fe3cbbfb9fa2ab55acbd3a3254d4378c81f4bef4392b1b18e91f10`  
		Last Modified: Mon, 31 Mar 2025 20:07:44 GMT  
		Size: 10.6 KB (10613 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.1-binary-linux` - linux; s390x

```console
$ docker pull nats@sha256:6b9323c60c161cbd82daa5b02f46e55051f8540e7c9770dc1c2ed619086c6f53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6122555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb48b95165c0163d0de0d793f09fa9aaa8dbc79c4b50241ee9e33ac819b1a501`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:cdb5d3b73d4e5760c377e2d1a31f668fd95251ac45157f6a4c4d98139b337e23`  
		Last Modified: Mon, 31 Mar 2025 17:41:31 GMT  
		Size: 6.1 MB (6122046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16e9431fd0e418054b688573b0ef6c205ce09bcb9015c474b01a32d6800912d0`  
		Last Modified: Mon, 31 Mar 2025 20:07:36 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.1-binary-linux` - unknown; unknown

```console
$ docker pull nats@sha256:2dfb1482f9d33c4a0f01a77e40b206f5b997b290b5e3899ee0c2678dd35731a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff58880fe981b8b31c473e8e992460d1ef7a218db9dd4ffc3a951750055bfd3`

```dockerfile
```

-	Layers:
	-	`sha256:9bb52fda18a732bf8f1ead6cd17dd200cfcae43fd84710a4ddb71372c0815f2b`  
		Last Modified: Mon, 31 Mar 2025 20:07:36 GMT  
		Size: 10.5 KB (10523 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.11.1-binary-nanoserver`

```console
$ docker pull nats@sha256:ab7919f36b0bf7f8b85e92aadeb04b95a0f3a5f1d2b33203d2ed60c8104ef5ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `nats:2.11.1-binary-nanoserver` - windows version 10.0.17763.7009; amd64

```console
$ docker pull nats@sha256:7523855e64c122a386122c97e7e122f78929c93ef1aaeabcfb818f96108eb526
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.4 MB (113369799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59c769ae1c19e869c3ab50a8bcc53b7a416139faa1f967bef29391891ff94a43`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 05 Mar 2025 21:54:26 GMT
RUN Apply image 10.0.17763.7009
# Mon, 31 Mar 2025 19:16:51 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Mon, 31 Mar 2025 19:16:54 GMT
RUN cmd /S /C #(nop) COPY file:cbd316e46d1e3baa5a0ffb6e227be5b521aa07a7cbe3a0513c0076ac28429bf3 in C:\nats-server.exe 
# Mon, 31 Mar 2025 19:16:55 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Mon, 31 Mar 2025 19:16:55 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Mon, 31 Mar 2025 19:16:56 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 31 Mar 2025 19:16:56 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:543388a101bf4d470af7e8817eff3f6f3b98f13d106939ab3f507a28f2825d0a`  
		Last Modified: Tue, 11 Mar 2025 22:40:48 GMT  
		Size: 106.9 MB (106907688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5764592bce5a260f59c0fc8af513aa702c03e73d61b9d9769cfb463cb5d345a4`  
		Last Modified: Mon, 31 Mar 2025 19:17:00 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c220ae7f5568ad8b19e77200fe2ab8b43bd7e66c8215b73f18cab048bf4c949b`  
		Last Modified: Mon, 31 Mar 2025 19:16:59 GMT  
		Size: 6.5 MB (6456094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24b9abd521fc3bf26173541357dca364e2aaa425fa95150aa12063ad86adbd0f`  
		Last Modified: Mon, 31 Mar 2025 19:16:59 GMT  
		Size: 1.7 KB (1684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47263123c2dca13a6ccd5e6c3f836df870102b1186585b3533a50841169f2d5d`  
		Last Modified: Mon, 31 Mar 2025 19:16:59 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb4c62df8bd6d5f27aca099be80d7290759022e9ed845409d9608b11f0e3db16`  
		Last Modified: Mon, 31 Mar 2025 19:16:58 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faf623903ff066d1e92e2c9250d8f7cd5a3230c1ea39d9cbe269fd63e735f4be`  
		Last Modified: Mon, 31 Mar 2025 19:16:59 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11.1-binary-nanoserver-1809`

```console
$ docker pull nats@sha256:ab7919f36b0bf7f8b85e92aadeb04b95a0f3a5f1d2b33203d2ed60c8104ef5ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `nats:2.11.1-binary-nanoserver-1809` - windows version 10.0.17763.7009; amd64

```console
$ docker pull nats@sha256:7523855e64c122a386122c97e7e122f78929c93ef1aaeabcfb818f96108eb526
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.4 MB (113369799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59c769ae1c19e869c3ab50a8bcc53b7a416139faa1f967bef29391891ff94a43`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 05 Mar 2025 21:54:26 GMT
RUN Apply image 10.0.17763.7009
# Mon, 31 Mar 2025 19:16:51 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Mon, 31 Mar 2025 19:16:54 GMT
RUN cmd /S /C #(nop) COPY file:cbd316e46d1e3baa5a0ffb6e227be5b521aa07a7cbe3a0513c0076ac28429bf3 in C:\nats-server.exe 
# Mon, 31 Mar 2025 19:16:55 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Mon, 31 Mar 2025 19:16:55 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Mon, 31 Mar 2025 19:16:56 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 31 Mar 2025 19:16:56 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:543388a101bf4d470af7e8817eff3f6f3b98f13d106939ab3f507a28f2825d0a`  
		Last Modified: Tue, 11 Mar 2025 22:40:48 GMT  
		Size: 106.9 MB (106907688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5764592bce5a260f59c0fc8af513aa702c03e73d61b9d9769cfb463cb5d345a4`  
		Last Modified: Mon, 31 Mar 2025 19:17:00 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c220ae7f5568ad8b19e77200fe2ab8b43bd7e66c8215b73f18cab048bf4c949b`  
		Last Modified: Mon, 31 Mar 2025 19:16:59 GMT  
		Size: 6.5 MB (6456094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24b9abd521fc3bf26173541357dca364e2aaa425fa95150aa12063ad86adbd0f`  
		Last Modified: Mon, 31 Mar 2025 19:16:59 GMT  
		Size: 1.7 KB (1684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47263123c2dca13a6ccd5e6c3f836df870102b1186585b3533a50841169f2d5d`  
		Last Modified: Mon, 31 Mar 2025 19:16:59 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb4c62df8bd6d5f27aca099be80d7290759022e9ed845409d9608b11f0e3db16`  
		Last Modified: Mon, 31 Mar 2025 19:16:58 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faf623903ff066d1e92e2c9250d8f7cd5a3230c1ea39d9cbe269fd63e735f4be`  
		Last Modified: Mon, 31 Mar 2025 19:16:59 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11.1-binary-scratch`

```console
$ docker pull nats@sha256:c81104c29f774ab6ac6178391029a857ca1b201750c9ebefad70bee0b9162cf6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.11.1-binary-scratch` - linux; amd64

```console
$ docker pull nats@sha256:0b313c16824b8d98736c06153fa01af3c8d62eebc6298e9062fd2e00c0a3e865
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6282666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5a2333da61b6c9f0de1de8235aca52ee071283b0c8c6487d3ea15b4a0f9f8e2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:54120e60f5a574cbbfd83de2711330ae98499a27ff592bdb694994b87749dd23`  
		Last Modified: Mon, 31 Mar 2025 17:41:30 GMT  
		Size: 6.3 MB (6282155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71d71c31c70e45e814d8db85102321f1459be653c595cd91fafb76306cdf405e`  
		Last Modified: Mon, 31 Mar 2025 19:07:36 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.1-binary-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:b8d62bc797363d5eab76aea96ec144d02b901da4dba8eb8bf31cc4e51e3a09d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbd51cd5b25ea5c4355cd2cde0e286d4f6da98802af9ed8b477001ff7ece4679`

```dockerfile
```

-	Layers:
	-	`sha256:19abc39a4cbb247bfa12363ce59bbce1e3bf861fddb9055c3a17e2d39d54d204`  
		Last Modified: Mon, 31 Mar 2025 19:07:36 GMT  
		Size: 10.5 KB (10523 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.1-binary-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:af5758489c2981e0a1028dc47f82f0dd2d26e2fac7ac1e478a2a15a12029f6d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6002169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c17f13cf88d7cb6d029eafd34cd847cbacebb2131dc5b7ecfbed791e2958e6a4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:098bda892a4e7ddd77ca838f72ef9757e9b3cfae3c7bc97076a8dd0b6fd92597`  
		Last Modified: Mon, 31 Mar 2025 17:41:30 GMT  
		Size: 6.0 MB (6001660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff1d2651842734b21329c25e1004a4da19102e57001381e60bb4fd58723fe19`  
		Last Modified: Mon, 31 Mar 2025 19:07:08 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.1-binary-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:736b8ee8472809de9731d9c426d2113e533e5ac68c9fbf4cd6bb44eb636b3d79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ffa52afcf9f827961f6f692daeb94f398721ac7559f559d56147558f6742150`

```dockerfile
```

-	Layers:
	-	`sha256:cc5887e8b88d73925b5364f9143ca37566f003a1560dffe173f7be8f10d66806`  
		Last Modified: Mon, 31 Mar 2025 19:07:08 GMT  
		Size: 10.7 KB (10650 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.1-binary-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:f1752b6d8b3a5506fab1fdf93ce66a6bd6e934d33a3c230231458f254ff505a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5992492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68d3d700cbec0d68868397c08f331e9cee8a3e484035ab651de2414c1bc1039b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7ae07ef7aadc186e26516a3b1a5bacd27b42c41b8d63efc540622587ef29be07`  
		Last Modified: Mon, 31 Mar 2025 17:41:36 GMT  
		Size: 6.0 MB (5991983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d132fb7bc19f6f368e535b5a46903e88d661e5c0f5e33c79b7d66b962039598`  
		Last Modified: Mon, 31 Mar 2025 20:44:23 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.1-binary-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:ff00ada993e928a0dbcd0e627e845b5f9c4d11042f0e089912b8ef2969c89876
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab26b373d46f30d56fc9b9ecf02d3c518eb5ab041a8fbb69e562b49b1a864d9d`

```dockerfile
```

-	Layers:
	-	`sha256:d552b4d64ce37965149a8aaeed3a0eebd251066efc77cb63ad2307f9d0bbdef7`  
		Last Modified: Mon, 31 Mar 2025 20:44:23 GMT  
		Size: 10.6 KB (10649 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.1-binary-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a360fbbfeb6f19012e875675cf70ea15e5ea3d9e003d5ccf1a61adeed8d515c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5776951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aad8d86003a865c09c995830bd52c9154c44e7976be35a0790b217a28445c6c2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:813138f2f23c3f67c00cc3f899e890b4b46ad187b3c70730ab91bd63ff37fa6d`  
		Last Modified: Mon, 31 Mar 2025 17:41:30 GMT  
		Size: 5.8 MB (5776442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d132fb7bc19f6f368e535b5a46903e88d661e5c0f5e33c79b7d66b962039598`  
		Last Modified: Mon, 31 Mar 2025 20:44:23 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.1-binary-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:13fe1989809a4185209660bba2e8a407b921e80a959889e94c8d6b18e6eadc66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cebd7eb7627ea55d24e6c1b36e5124796e00e1a2243414d5b3f65ff44089ec66`

```dockerfile
```

-	Layers:
	-	`sha256:a33f391d8364f479953478aa1b1ce3f8e6e05c31407e5d9ead5d4d5db6da559f`  
		Last Modified: Mon, 31 Mar 2025 20:44:29 GMT  
		Size: 10.7 KB (10708 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.1-binary-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:74e2df57ac704452ee531238216b3accd76025199ee310563732dd2c680227a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5757216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abd71cf45edbcaea354422b03a686d602fac79be9357fdbc6b5c05d8ab8309e5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:452917a8c6e0add88a19efed21ff3bf850d722622f476c3b9d4426f3dbaaffb7`  
		Last Modified: Mon, 31 Mar 2025 17:41:27 GMT  
		Size: 5.8 MB (5756706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc09a85b63b7a6867f196c8c27905ad711a7457fa91d3df80022bc3d24111b3`  
		Last Modified: Mon, 31 Mar 2025 20:07:44 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.1-binary-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:9460476db24c3ccd45c6374ab5e0dfa8af2b95e6ed003b294fca69a3f6d49e72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8048c19445dcae5f87494cedbc4822265fb6848963d3958920bc8a77dc19881`

```dockerfile
```

-	Layers:
	-	`sha256:2e79f43f61fe3cbbfb9fa2ab55acbd3a3254d4378c81f4bef4392b1b18e91f10`  
		Last Modified: Mon, 31 Mar 2025 20:07:44 GMT  
		Size: 10.6 KB (10613 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.1-binary-scratch` - linux; s390x

```console
$ docker pull nats@sha256:6b9323c60c161cbd82daa5b02f46e55051f8540e7c9770dc1c2ed619086c6f53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6122555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb48b95165c0163d0de0d793f09fa9aaa8dbc79c4b50241ee9e33ac819b1a501`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:cdb5d3b73d4e5760c377e2d1a31f668fd95251ac45157f6a4c4d98139b337e23`  
		Last Modified: Mon, 31 Mar 2025 17:41:31 GMT  
		Size: 6.1 MB (6122046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16e9431fd0e418054b688573b0ef6c205ce09bcb9015c474b01a32d6800912d0`  
		Last Modified: Mon, 31 Mar 2025 20:07:36 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.1-binary-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:2dfb1482f9d33c4a0f01a77e40b206f5b997b290b5e3899ee0c2678dd35731a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff58880fe981b8b31c473e8e992460d1ef7a218db9dd4ffc3a951750055bfd3`

```dockerfile
```

-	Layers:
	-	`sha256:9bb52fda18a732bf8f1ead6cd17dd200cfcae43fd84710a4ddb71372c0815f2b`  
		Last Modified: Mon, 31 Mar 2025 20:07:36 GMT  
		Size: 10.5 KB (10523 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.11.1-binary-windowsservercore`

```console
$ docker pull nats@sha256:9d03bcf6cbd1a06b72b01b12931276f9f11d428800308790ac7d2c5e7f013153
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `nats:2.11.1-binary-windowsservercore` - windows version 10.0.17763.7009; amd64

```console
$ docker pull nats@sha256:358cd0aed79a204ff4c8b5c055a03c487c5358d7455e0ffa579125eceef0d34e
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2158788658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ee73222ac79929936f4b58dc26a22b9521b1d61e7a78f7c5ed88a75f23f1374`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 05 Mar 2025 22:09:20 GMT
RUN Install update 10.0.17763.7009
# Mon, 31 Mar 2025 18:52:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 31 Mar 2025 18:52:57 GMT
ENV NATS_DOCKERIZED=1
# Mon, 31 Mar 2025 18:52:58 GMT
ENV NATS_SERVER=2.11.1-binary
# Mon, 31 Mar 2025 18:52:59 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.1-binary/nats-server-v2.11.1-binary-windows-amd64.zip
# Mon, 31 Mar 2025 18:52:59 GMT
ENV NATS_SERVER_SHASUM=2ab6b2c964fd5fe3b10a471cba309033f0756182f69228a65d1764197facf59c
# Mon, 31 Mar 2025 18:53:46 GMT
RUN Set-PSDebug -Trace 2
# Mon, 31 Mar 2025 18:54:06 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Mon, 31 Mar 2025 18:54:06 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Mon, 31 Mar 2025 18:54:07 GMT
EXPOSE 4222 6222 8222
# Mon, 31 Mar 2025 18:54:08 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 31 Mar 2025 18:54:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77bec5e4bac3c7f6dc5d56da5ffc11e72881485b3a55330c17c915ad653f955`  
		Last Modified: Tue, 11 Mar 2025 17:48:06 GMT  
		Size: 431.4 MB (431366277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35a6c48e83b6ecc670f12e09411b9f19d7fb0a878e1f86a6812563467340ff8`  
		Last Modified: Mon, 31 Mar 2025 18:54:13 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c158e67ae1fa853b1e146c6dd4e2b8f7e13aab94075904e788f4dfa3b8943322`  
		Last Modified: Mon, 31 Mar 2025 18:54:12 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6610f67e82d540d4cf11d12f87f1a68f8b42e4371905c52df1cade737e4f44c`  
		Last Modified: Mon, 31 Mar 2025 18:54:11 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0929886be3ca1628c185214c762369ea53c4afb47d0603d3d69fb4b471d01bf7`  
		Last Modified: Mon, 31 Mar 2025 18:54:12 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a89f7e18c6f6e8406fbe811630282ddd985e8899085b73506a0f39ac3c8fcf33`  
		Last Modified: Mon, 31 Mar 2025 18:54:11 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a904ed39f5ad31d12b93284fed611d377be64b1d3871e896c2e1c83415ff28`  
		Last Modified: Mon, 31 Mar 2025 18:54:11 GMT  
		Size: 333.8 KB (333807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5239d01ea32c2be9edfc2b25b142685efcbaedbadb1778166b52c0858df66464`  
		Last Modified: Mon, 31 Mar 2025 18:54:11 GMT  
		Size: 6.8 MB (6807873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56c6af05e936d2967cd915bd57f5faacef8b514317cd4de730f837f728d14487`  
		Last Modified: Mon, 31 Mar 2025 18:54:10 GMT  
		Size: 1.9 KB (1931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe56937824b786b5d064fe15be3435e14f26a022d00662003396c61194954e0`  
		Last Modified: Mon, 31 Mar 2025 18:54:10 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4aaffd9d1722fd09e9a67ad18073b6716178658c1f5517404d7b4180df3142f`  
		Last Modified: Mon, 31 Mar 2025 18:54:10 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdcbf0f98ff7504665d65ee0034ca94a89e45d2ecc47f808f87787d51427d265`  
		Last Modified: Mon, 31 Mar 2025 18:54:10 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11.1-binary-windowsservercore-1809`

```console
$ docker pull nats@sha256:9d03bcf6cbd1a06b72b01b12931276f9f11d428800308790ac7d2c5e7f013153
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `nats:2.11.1-binary-windowsservercore-1809` - windows version 10.0.17763.7009; amd64

```console
$ docker pull nats@sha256:358cd0aed79a204ff4c8b5c055a03c487c5358d7455e0ffa579125eceef0d34e
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2158788658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ee73222ac79929936f4b58dc26a22b9521b1d61e7a78f7c5ed88a75f23f1374`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 05 Mar 2025 22:09:20 GMT
RUN Install update 10.0.17763.7009
# Mon, 31 Mar 2025 18:52:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 31 Mar 2025 18:52:57 GMT
ENV NATS_DOCKERIZED=1
# Mon, 31 Mar 2025 18:52:58 GMT
ENV NATS_SERVER=2.11.1-binary
# Mon, 31 Mar 2025 18:52:59 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.1-binary/nats-server-v2.11.1-binary-windows-amd64.zip
# Mon, 31 Mar 2025 18:52:59 GMT
ENV NATS_SERVER_SHASUM=2ab6b2c964fd5fe3b10a471cba309033f0756182f69228a65d1764197facf59c
# Mon, 31 Mar 2025 18:53:46 GMT
RUN Set-PSDebug -Trace 2
# Mon, 31 Mar 2025 18:54:06 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Mon, 31 Mar 2025 18:54:06 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Mon, 31 Mar 2025 18:54:07 GMT
EXPOSE 4222 6222 8222
# Mon, 31 Mar 2025 18:54:08 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 31 Mar 2025 18:54:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77bec5e4bac3c7f6dc5d56da5ffc11e72881485b3a55330c17c915ad653f955`  
		Last Modified: Tue, 11 Mar 2025 17:48:06 GMT  
		Size: 431.4 MB (431366277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35a6c48e83b6ecc670f12e09411b9f19d7fb0a878e1f86a6812563467340ff8`  
		Last Modified: Mon, 31 Mar 2025 18:54:13 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c158e67ae1fa853b1e146c6dd4e2b8f7e13aab94075904e788f4dfa3b8943322`  
		Last Modified: Mon, 31 Mar 2025 18:54:12 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6610f67e82d540d4cf11d12f87f1a68f8b42e4371905c52df1cade737e4f44c`  
		Last Modified: Mon, 31 Mar 2025 18:54:11 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0929886be3ca1628c185214c762369ea53c4afb47d0603d3d69fb4b471d01bf7`  
		Last Modified: Mon, 31 Mar 2025 18:54:12 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a89f7e18c6f6e8406fbe811630282ddd985e8899085b73506a0f39ac3c8fcf33`  
		Last Modified: Mon, 31 Mar 2025 18:54:11 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a904ed39f5ad31d12b93284fed611d377be64b1d3871e896c2e1c83415ff28`  
		Last Modified: Mon, 31 Mar 2025 18:54:11 GMT  
		Size: 333.8 KB (333807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5239d01ea32c2be9edfc2b25b142685efcbaedbadb1778166b52c0858df66464`  
		Last Modified: Mon, 31 Mar 2025 18:54:11 GMT  
		Size: 6.8 MB (6807873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56c6af05e936d2967cd915bd57f5faacef8b514317cd4de730f837f728d14487`  
		Last Modified: Mon, 31 Mar 2025 18:54:10 GMT  
		Size: 1.9 KB (1931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe56937824b786b5d064fe15be3435e14f26a022d00662003396c61194954e0`  
		Last Modified: Mon, 31 Mar 2025 18:54:10 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4aaffd9d1722fd09e9a67ad18073b6716178658c1f5517404d7b4180df3142f`  
		Last Modified: Mon, 31 Mar 2025 18:54:10 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdcbf0f98ff7504665d65ee0034ca94a89e45d2ecc47f808f87787d51427d265`  
		Last Modified: Mon, 31 Mar 2025 18:54:10 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine`

```console
$ docker pull nats@sha256:222b8a7f2b9cbef1a51d412a5782ee75eac04062413d61c960b051e29c214115
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:alpine` - linux; amd64

```console
$ docker pull nats@sha256:d2bfc2b0b53f2a35c4b1c6fb432695b13dd232bdb551ea62c9fc00148520401f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10386128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6a871a4d4c93dc7e032ef72a3a722439e2ce32e96063585474891c6b654043f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
ENV NATS_SERVER=2.11.1-binary
# Mon, 31 Mar 2025 17:39:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='2499105f9e64bef55f168f634d34a586b710f6ac041639d8a18364f2b4f4c410' ;; 		armhf) natsArch='arm6'; sha256='31bc11906458e30c8028cdd0301de98713074db73f5e352f58ce4ecd6b1cc641' ;; 		armv7) natsArch='arm7'; sha256='432f4c47cf5adca05da67f1feaf969f6cea50ed9c3bb743a8bb76b8c5c583c8e' ;; 		x86_64) natsArch='amd64'; sha256='827497f99acd54eb0e4e8bfa3b0eb31dd51c6c259110de11a45a7fdacae6c5b3' ;; 		x86) natsArch='386'; sha256='651065e2170ee0f7e244425c0d0ba30a38776a7aef75e2d5cba0b8b11a950c54' ;; 		s390x) natsArch='s390x'; sha256='23e6ce6b70f9b973106d325eebb8bdd613040bedd4da980ff0aea2d2a7dc122e' ;; 		ppc64le) natsArch='ppc64le'; sha256='5341f41ef6298b05b72dd77c1ec055aeacb1b57dfd600ec888317347b3b4cbf8' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0643a146757fce88425f18db35388da5f1441b9e655395106fc3b6de8f7779a`  
		Last Modified: Mon, 31 Mar 2025 18:43:34 GMT  
		Size: 6.7 MB (6742912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f810863f848d47b0ec90164d81013c3f49b7d5d94bf9c42a73558dc7c46cfce`  
		Last Modified: Mon, 31 Mar 2025 18:43:33 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3295cd3199e071474b886bbbcf41ef4c12302ddbe5f1bd9283c8e119abcefe39`  
		Last Modified: Mon, 31 Mar 2025 18:43:33 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:7a817ee3d7045d87d4f49299e408201d1118ee221fdda63c5b66733871a32dea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89e54e9039e9d3c99605b12728bbecef9c9479593bdf67a68e894df9ecba60c4`

```dockerfile
```

-	Layers:
	-	`sha256:d380a2bbbdfb0718224f60b142dc29624483f0d28fa0552fb8e915ab9c1d69d2`  
		Last Modified: Mon, 31 Mar 2025 18:43:33 GMT  
		Size: 14.4 KB (14360 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:5b003eca587d5d1ded87d52f52a88b49c6091e2ae6ffcbcc9591ef31edfb1153
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9830711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd78fe0bc28317f1acadcd3ed9a09443a843f5cf68ef058de361ff0570543e01`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
ENV NATS_SERVER=2.11.1-binary
# Mon, 31 Mar 2025 17:39:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='2499105f9e64bef55f168f634d34a586b710f6ac041639d8a18364f2b4f4c410' ;; 		armhf) natsArch='arm6'; sha256='31bc11906458e30c8028cdd0301de98713074db73f5e352f58ce4ecd6b1cc641' ;; 		armv7) natsArch='arm7'; sha256='432f4c47cf5adca05da67f1feaf969f6cea50ed9c3bb743a8bb76b8c5c583c8e' ;; 		x86_64) natsArch='amd64'; sha256='827497f99acd54eb0e4e8bfa3b0eb31dd51c6c259110de11a45a7fdacae6c5b3' ;; 		x86) natsArch='386'; sha256='651065e2170ee0f7e244425c0d0ba30a38776a7aef75e2d5cba0b8b11a950c54' ;; 		s390x) natsArch='s390x'; sha256='23e6ce6b70f9b973106d325eebb8bdd613040bedd4da980ff0aea2d2a7dc122e' ;; 		ppc64le) natsArch='ppc64le'; sha256='5341f41ef6298b05b72dd77c1ec055aeacb1b57dfd600ec888317347b3b4cbf8' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c92f9bdc82b0d8955653988d31a42d2d808133d9b313a6f16c7c1fc6187ce7c3`  
		Last Modified: Mon, 31 Mar 2025 18:50:14 GMT  
		Size: 6.5 MB (6465008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f8f3e30080f28fb154a8574bfa9e68094196baa500cc70232b4b6a993d7d96`  
		Last Modified: Mon, 31 Mar 2025 18:50:13 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b07ed84ffecb4fe35014c6ec28f044236b811f87738a6e32d50061b6cdcf8913`  
		Last Modified: Mon, 31 Mar 2025 18:50:13 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:25ca21f30fda2b87f68ede801458791fdf7fb7571b1dfc4c5b92a80f7287b667
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fa2e55e1097547a0c5dc17d479d5b338734fce9c9e83240bf6a9eb19569188a`

```dockerfile
```

-	Layers:
	-	`sha256:f659982640e897f8f52e71b1b320e9ea56d5354063a38cf666928fe3ccf97400`  
		Last Modified: Mon, 31 Mar 2025 18:50:13 GMT  
		Size: 14.5 KB (14468 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:f6f902d9d220b13f8c52befb0e4f2520a530e999e9d0d7e3b4a7c96d1d6a2d4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9552225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f49a7e1e59161babacc6a62e07238abd7b349a8efc80a4bfd1523785ae8ece72`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
ENV NATS_SERVER=2.11.1-binary
# Mon, 31 Mar 2025 17:39:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='2499105f9e64bef55f168f634d34a586b710f6ac041639d8a18364f2b4f4c410' ;; 		armhf) natsArch='arm6'; sha256='31bc11906458e30c8028cdd0301de98713074db73f5e352f58ce4ecd6b1cc641' ;; 		armv7) natsArch='arm7'; sha256='432f4c47cf5adca05da67f1feaf969f6cea50ed9c3bb743a8bb76b8c5c583c8e' ;; 		x86_64) natsArch='amd64'; sha256='827497f99acd54eb0e4e8bfa3b0eb31dd51c6c259110de11a45a7fdacae6c5b3' ;; 		x86) natsArch='386'; sha256='651065e2170ee0f7e244425c0d0ba30a38776a7aef75e2d5cba0b8b11a950c54' ;; 		s390x) natsArch='s390x'; sha256='23e6ce6b70f9b973106d325eebb8bdd613040bedd4da980ff0aea2d2a7dc122e' ;; 		ppc64le) natsArch='ppc64le'; sha256='5341f41ef6298b05b72dd77c1ec055aeacb1b57dfd600ec888317347b3b4cbf8' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4be7f6d278a4174ef17dcd8c89848f067134976f430004cbed069643b89e46e8`  
		Last Modified: Mon, 31 Mar 2025 20:17:05 GMT  
		Size: 6.5 MB (6453133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825c724725f466486a81cdde1ec6a92840eb03f19fc7c9f6c2361d13f3398293`  
		Last Modified: Mon, 31 Mar 2025 20:17:04 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe87685444a72475e87e5ffbb1baff8c65017859e8e53c72573fc546273e8ef6`  
		Last Modified: Mon, 31 Mar 2025 20:17:04 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:860dd6d0c495dc91deb8a4c27e98247c01e7cc5ba0a4a80d0e33430aaa5695db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41756094504db64ff2b19360c941882401645db6e11cb7b116c9cc5d965c1002`

```dockerfile
```

-	Layers:
	-	`sha256:a83dd1e9193bcbd50a20cfab9ac07e63cb0d3f71b71000fc9b9e4456a63ddc2c`  
		Last Modified: Mon, 31 Mar 2025 20:17:04 GMT  
		Size: 14.5 KB (14468 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:90874ce66332c5ed35925509121cc1231be38266af7f5efe7097f37a54610dc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10234990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e934c9514dbf2966156ca2a5b60a8c62eab86a1d0e9316d96e587bc52837aff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
ENV NATS_SERVER=2.11.1-binary
# Mon, 31 Mar 2025 17:39:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='2499105f9e64bef55f168f634d34a586b710f6ac041639d8a18364f2b4f4c410' ;; 		armhf) natsArch='arm6'; sha256='31bc11906458e30c8028cdd0301de98713074db73f5e352f58ce4ecd6b1cc641' ;; 		armv7) natsArch='arm7'; sha256='432f4c47cf5adca05da67f1feaf969f6cea50ed9c3bb743a8bb76b8c5c583c8e' ;; 		x86_64) natsArch='amd64'; sha256='827497f99acd54eb0e4e8bfa3b0eb31dd51c6c259110de11a45a7fdacae6c5b3' ;; 		x86) natsArch='386'; sha256='651065e2170ee0f7e244425c0d0ba30a38776a7aef75e2d5cba0b8b11a950c54' ;; 		s390x) natsArch='s390x'; sha256='23e6ce6b70f9b973106d325eebb8bdd613040bedd4da980ff0aea2d2a7dc122e' ;; 		ppc64le) natsArch='ppc64le'; sha256='5341f41ef6298b05b72dd77c1ec055aeacb1b57dfd600ec888317347b3b4cbf8' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60797fdb0b4d910be869065ae81ab51200fbe5544785eb4efa8fc7cb9eb3033e`  
		Last Modified: Mon, 31 Mar 2025 20:11:13 GMT  
		Size: 6.2 MB (6240991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dda5bbcac3d56d1f2414331f89b9333ef3393083b91ce07a2face8802428335`  
		Last Modified: Mon, 31 Mar 2025 20:11:12 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c42e24e15c065a92a28be68d337a0e3f21fc9b4bee9e5e931179ab16a647031`  
		Last Modified: Mon, 31 Mar 2025 20:11:12 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:061fa681d240f27b08e83d14d855bff8191035c3944adf647afab28af9d67b5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a76bc64a67b68410441588e0e8ebc82c70ec9260099bfb6d4d5154152785d62`

```dockerfile
```

-	Layers:
	-	`sha256:5b3a7763692c9fffeebb31f53b8a14d7192250292c1661653d8912d27e67bd34`  
		Last Modified: Mon, 31 Mar 2025 20:11:12 GMT  
		Size: 14.5 KB (14512 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:f09b96d5bfacda0649814f91facba68b0ecca96de4ebdea7e17dfde79f1ada96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9796685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10c6bb2aed5161b870f53898cce57635999f3e6368d89209be712832cb7caae3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
ENV NATS_SERVER=2.11.1-binary
# Mon, 31 Mar 2025 17:39:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='2499105f9e64bef55f168f634d34a586b710f6ac041639d8a18364f2b4f4c410' ;; 		armhf) natsArch='arm6'; sha256='31bc11906458e30c8028cdd0301de98713074db73f5e352f58ce4ecd6b1cc641' ;; 		armv7) natsArch='arm7'; sha256='432f4c47cf5adca05da67f1feaf969f6cea50ed9c3bb743a8bb76b8c5c583c8e' ;; 		x86_64) natsArch='amd64'; sha256='827497f99acd54eb0e4e8bfa3b0eb31dd51c6c259110de11a45a7fdacae6c5b3' ;; 		x86) natsArch='386'; sha256='651065e2170ee0f7e244425c0d0ba30a38776a7aef75e2d5cba0b8b11a950c54' ;; 		s390x) natsArch='s390x'; sha256='23e6ce6b70f9b973106d325eebb8bdd613040bedd4da980ff0aea2d2a7dc122e' ;; 		ppc64le) natsArch='ppc64le'; sha256='5341f41ef6298b05b72dd77c1ec055aeacb1b57dfd600ec888317347b3b4cbf8' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:299c0ee564e4568e71d43a566874e9d853458071d554386ad5728913e55f5d42`  
		Last Modified: Mon, 31 Mar 2025 19:45:06 GMT  
		Size: 6.2 MB (6221370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1af98871a1453d715b201d0cb6c30c2e8240dd12ee7af67f4334bfb80877f3bb`  
		Last Modified: Mon, 31 Mar 2025 19:45:05 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:103d308786c4f17ef7f21746eadc69443e28518b33fd5534040a513bbb5acc64`  
		Last Modified: Mon, 31 Mar 2025 19:45:05 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:261ca6909da20cd9b36804c44211d5a257a4f0a8746e425a8d63cebe1ff274eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bf43f070134532bf9419111138ee6504a3b9010b90d59e6380375b5b9a4abcf`

```dockerfile
```

-	Layers:
	-	`sha256:09877c6dec89674d2ec4aefc8edd75ff573a4834ca2851e1a4be89994ffcd528`  
		Last Modified: Mon, 31 Mar 2025 19:45:05 GMT  
		Size: 14.4 KB (14427 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; s390x

```console
$ docker pull nats@sha256:c14e89986785ed37ac2931d4b307ea84375f49180341e48c9024fe40f226decc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10053962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:893690471f61ea43e10126b7ceb4fd7a07fd98eb86fff95edc6cd8cf10d1e4ef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
ENV NATS_SERVER=2.11.1-binary
# Mon, 31 Mar 2025 17:39:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='2499105f9e64bef55f168f634d34a586b710f6ac041639d8a18364f2b4f4c410' ;; 		armhf) natsArch='arm6'; sha256='31bc11906458e30c8028cdd0301de98713074db73f5e352f58ce4ecd6b1cc641' ;; 		armv7) natsArch='arm7'; sha256='432f4c47cf5adca05da67f1feaf969f6cea50ed9c3bb743a8bb76b8c5c583c8e' ;; 		x86_64) natsArch='amd64'; sha256='827497f99acd54eb0e4e8bfa3b0eb31dd51c6c259110de11a45a7fdacae6c5b3' ;; 		x86) natsArch='386'; sha256='651065e2170ee0f7e244425c0d0ba30a38776a7aef75e2d5cba0b8b11a950c54' ;; 		s390x) natsArch='s390x'; sha256='23e6ce6b70f9b973106d325eebb8bdd613040bedd4da980ff0aea2d2a7dc122e' ;; 		ppc64le) natsArch='ppc64le'; sha256='5341f41ef6298b05b72dd77c1ec055aeacb1b57dfd600ec888317347b3b4cbf8' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67f000d40cf6813dabcb134d2a9b15f3b7eb5ba7dba583ad1df023b35efd9ca`  
		Last Modified: Mon, 31 Mar 2025 19:28:46 GMT  
		Size: 6.6 MB (6585424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4501a9ec92d7d9a89fd0e10cd2ba4c8fb93658a4d46301543d45d1f96b07ce32`  
		Last Modified: Mon, 31 Mar 2025 19:28:45 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06c2b65e72a2a266d2d783396559cd0ee8346a11e25f65ca2b21cc82de4174b6`  
		Last Modified: Mon, 31 Mar 2025 19:28:45 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:82ec15847478c49a8a561d7f21d2239bbea2614e277659456213e6bdd0f5dd49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:443d1aa445d5406aada9c0970885e837d983ea976af12760bad0de2704481f16`

```dockerfile
```

-	Layers:
	-	`sha256:688e4b2d5f0fdef107c3405864e3c9cc14ae13fd320ceddce8f4667dcde9d786`  
		Last Modified: Mon, 31 Mar 2025 19:28:45 GMT  
		Size: 14.4 KB (14360 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:alpine3.21`

```console
$ docker pull nats@sha256:222b8a7f2b9cbef1a51d412a5782ee75eac04062413d61c960b051e29c214115
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:alpine3.21` - linux; amd64

```console
$ docker pull nats@sha256:d2bfc2b0b53f2a35c4b1c6fb432695b13dd232bdb551ea62c9fc00148520401f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10386128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6a871a4d4c93dc7e032ef72a3a722439e2ce32e96063585474891c6b654043f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
ENV NATS_SERVER=2.11.1-binary
# Mon, 31 Mar 2025 17:39:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='2499105f9e64bef55f168f634d34a586b710f6ac041639d8a18364f2b4f4c410' ;; 		armhf) natsArch='arm6'; sha256='31bc11906458e30c8028cdd0301de98713074db73f5e352f58ce4ecd6b1cc641' ;; 		armv7) natsArch='arm7'; sha256='432f4c47cf5adca05da67f1feaf969f6cea50ed9c3bb743a8bb76b8c5c583c8e' ;; 		x86_64) natsArch='amd64'; sha256='827497f99acd54eb0e4e8bfa3b0eb31dd51c6c259110de11a45a7fdacae6c5b3' ;; 		x86) natsArch='386'; sha256='651065e2170ee0f7e244425c0d0ba30a38776a7aef75e2d5cba0b8b11a950c54' ;; 		s390x) natsArch='s390x'; sha256='23e6ce6b70f9b973106d325eebb8bdd613040bedd4da980ff0aea2d2a7dc122e' ;; 		ppc64le) natsArch='ppc64le'; sha256='5341f41ef6298b05b72dd77c1ec055aeacb1b57dfd600ec888317347b3b4cbf8' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0643a146757fce88425f18db35388da5f1441b9e655395106fc3b6de8f7779a`  
		Last Modified: Mon, 31 Mar 2025 18:43:34 GMT  
		Size: 6.7 MB (6742912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f810863f848d47b0ec90164d81013c3f49b7d5d94bf9c42a73558dc7c46cfce`  
		Last Modified: Mon, 31 Mar 2025 18:43:33 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3295cd3199e071474b886bbbcf41ef4c12302ddbe5f1bd9283c8e119abcefe39`  
		Last Modified: Mon, 31 Mar 2025 18:43:33 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:7a817ee3d7045d87d4f49299e408201d1118ee221fdda63c5b66733871a32dea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89e54e9039e9d3c99605b12728bbecef9c9479593bdf67a68e894df9ecba60c4`

```dockerfile
```

-	Layers:
	-	`sha256:d380a2bbbdfb0718224f60b142dc29624483f0d28fa0552fb8e915ab9c1d69d2`  
		Last Modified: Mon, 31 Mar 2025 18:43:33 GMT  
		Size: 14.4 KB (14360 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.21` - linux; arm variant v6

```console
$ docker pull nats@sha256:5b003eca587d5d1ded87d52f52a88b49c6091e2ae6ffcbcc9591ef31edfb1153
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9830711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd78fe0bc28317f1acadcd3ed9a09443a843f5cf68ef058de361ff0570543e01`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
ENV NATS_SERVER=2.11.1-binary
# Mon, 31 Mar 2025 17:39:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='2499105f9e64bef55f168f634d34a586b710f6ac041639d8a18364f2b4f4c410' ;; 		armhf) natsArch='arm6'; sha256='31bc11906458e30c8028cdd0301de98713074db73f5e352f58ce4ecd6b1cc641' ;; 		armv7) natsArch='arm7'; sha256='432f4c47cf5adca05da67f1feaf969f6cea50ed9c3bb743a8bb76b8c5c583c8e' ;; 		x86_64) natsArch='amd64'; sha256='827497f99acd54eb0e4e8bfa3b0eb31dd51c6c259110de11a45a7fdacae6c5b3' ;; 		x86) natsArch='386'; sha256='651065e2170ee0f7e244425c0d0ba30a38776a7aef75e2d5cba0b8b11a950c54' ;; 		s390x) natsArch='s390x'; sha256='23e6ce6b70f9b973106d325eebb8bdd613040bedd4da980ff0aea2d2a7dc122e' ;; 		ppc64le) natsArch='ppc64le'; sha256='5341f41ef6298b05b72dd77c1ec055aeacb1b57dfd600ec888317347b3b4cbf8' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c92f9bdc82b0d8955653988d31a42d2d808133d9b313a6f16c7c1fc6187ce7c3`  
		Last Modified: Mon, 31 Mar 2025 18:50:14 GMT  
		Size: 6.5 MB (6465008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f8f3e30080f28fb154a8574bfa9e68094196baa500cc70232b4b6a993d7d96`  
		Last Modified: Mon, 31 Mar 2025 18:50:13 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b07ed84ffecb4fe35014c6ec28f044236b811f87738a6e32d50061b6cdcf8913`  
		Last Modified: Mon, 31 Mar 2025 18:50:13 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:25ca21f30fda2b87f68ede801458791fdf7fb7571b1dfc4c5b92a80f7287b667
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fa2e55e1097547a0c5dc17d479d5b338734fce9c9e83240bf6a9eb19569188a`

```dockerfile
```

-	Layers:
	-	`sha256:f659982640e897f8f52e71b1b320e9ea56d5354063a38cf666928fe3ccf97400`  
		Last Modified: Mon, 31 Mar 2025 18:50:13 GMT  
		Size: 14.5 KB (14468 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.21` - linux; arm variant v7

```console
$ docker pull nats@sha256:f6f902d9d220b13f8c52befb0e4f2520a530e999e9d0d7e3b4a7c96d1d6a2d4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9552225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f49a7e1e59161babacc6a62e07238abd7b349a8efc80a4bfd1523785ae8ece72`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
ENV NATS_SERVER=2.11.1-binary
# Mon, 31 Mar 2025 17:39:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='2499105f9e64bef55f168f634d34a586b710f6ac041639d8a18364f2b4f4c410' ;; 		armhf) natsArch='arm6'; sha256='31bc11906458e30c8028cdd0301de98713074db73f5e352f58ce4ecd6b1cc641' ;; 		armv7) natsArch='arm7'; sha256='432f4c47cf5adca05da67f1feaf969f6cea50ed9c3bb743a8bb76b8c5c583c8e' ;; 		x86_64) natsArch='amd64'; sha256='827497f99acd54eb0e4e8bfa3b0eb31dd51c6c259110de11a45a7fdacae6c5b3' ;; 		x86) natsArch='386'; sha256='651065e2170ee0f7e244425c0d0ba30a38776a7aef75e2d5cba0b8b11a950c54' ;; 		s390x) natsArch='s390x'; sha256='23e6ce6b70f9b973106d325eebb8bdd613040bedd4da980ff0aea2d2a7dc122e' ;; 		ppc64le) natsArch='ppc64le'; sha256='5341f41ef6298b05b72dd77c1ec055aeacb1b57dfd600ec888317347b3b4cbf8' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4be7f6d278a4174ef17dcd8c89848f067134976f430004cbed069643b89e46e8`  
		Last Modified: Mon, 31 Mar 2025 20:17:05 GMT  
		Size: 6.5 MB (6453133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825c724725f466486a81cdde1ec6a92840eb03f19fc7c9f6c2361d13f3398293`  
		Last Modified: Mon, 31 Mar 2025 20:17:04 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe87685444a72475e87e5ffbb1baff8c65017859e8e53c72573fc546273e8ef6`  
		Last Modified: Mon, 31 Mar 2025 20:17:04 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:860dd6d0c495dc91deb8a4c27e98247c01e7cc5ba0a4a80d0e33430aaa5695db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41756094504db64ff2b19360c941882401645db6e11cb7b116c9cc5d965c1002`

```dockerfile
```

-	Layers:
	-	`sha256:a83dd1e9193bcbd50a20cfab9ac07e63cb0d3f71b71000fc9b9e4456a63ddc2c`  
		Last Modified: Mon, 31 Mar 2025 20:17:04 GMT  
		Size: 14.5 KB (14468 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.21` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:90874ce66332c5ed35925509121cc1231be38266af7f5efe7097f37a54610dc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10234990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e934c9514dbf2966156ca2a5b60a8c62eab86a1d0e9316d96e587bc52837aff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
ENV NATS_SERVER=2.11.1-binary
# Mon, 31 Mar 2025 17:39:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='2499105f9e64bef55f168f634d34a586b710f6ac041639d8a18364f2b4f4c410' ;; 		armhf) natsArch='arm6'; sha256='31bc11906458e30c8028cdd0301de98713074db73f5e352f58ce4ecd6b1cc641' ;; 		armv7) natsArch='arm7'; sha256='432f4c47cf5adca05da67f1feaf969f6cea50ed9c3bb743a8bb76b8c5c583c8e' ;; 		x86_64) natsArch='amd64'; sha256='827497f99acd54eb0e4e8bfa3b0eb31dd51c6c259110de11a45a7fdacae6c5b3' ;; 		x86) natsArch='386'; sha256='651065e2170ee0f7e244425c0d0ba30a38776a7aef75e2d5cba0b8b11a950c54' ;; 		s390x) natsArch='s390x'; sha256='23e6ce6b70f9b973106d325eebb8bdd613040bedd4da980ff0aea2d2a7dc122e' ;; 		ppc64le) natsArch='ppc64le'; sha256='5341f41ef6298b05b72dd77c1ec055aeacb1b57dfd600ec888317347b3b4cbf8' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60797fdb0b4d910be869065ae81ab51200fbe5544785eb4efa8fc7cb9eb3033e`  
		Last Modified: Mon, 31 Mar 2025 20:11:13 GMT  
		Size: 6.2 MB (6240991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dda5bbcac3d56d1f2414331f89b9333ef3393083b91ce07a2face8802428335`  
		Last Modified: Mon, 31 Mar 2025 20:11:12 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c42e24e15c065a92a28be68d337a0e3f21fc9b4bee9e5e931179ab16a647031`  
		Last Modified: Mon, 31 Mar 2025 20:11:12 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:061fa681d240f27b08e83d14d855bff8191035c3944adf647afab28af9d67b5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a76bc64a67b68410441588e0e8ebc82c70ec9260099bfb6d4d5154152785d62`

```dockerfile
```

-	Layers:
	-	`sha256:5b3a7763692c9fffeebb31f53b8a14d7192250292c1661653d8912d27e67bd34`  
		Last Modified: Mon, 31 Mar 2025 20:11:12 GMT  
		Size: 14.5 KB (14512 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.21` - linux; ppc64le

```console
$ docker pull nats@sha256:f09b96d5bfacda0649814f91facba68b0ecca96de4ebdea7e17dfde79f1ada96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9796685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10c6bb2aed5161b870f53898cce57635999f3e6368d89209be712832cb7caae3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
ENV NATS_SERVER=2.11.1-binary
# Mon, 31 Mar 2025 17:39:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='2499105f9e64bef55f168f634d34a586b710f6ac041639d8a18364f2b4f4c410' ;; 		armhf) natsArch='arm6'; sha256='31bc11906458e30c8028cdd0301de98713074db73f5e352f58ce4ecd6b1cc641' ;; 		armv7) natsArch='arm7'; sha256='432f4c47cf5adca05da67f1feaf969f6cea50ed9c3bb743a8bb76b8c5c583c8e' ;; 		x86_64) natsArch='amd64'; sha256='827497f99acd54eb0e4e8bfa3b0eb31dd51c6c259110de11a45a7fdacae6c5b3' ;; 		x86) natsArch='386'; sha256='651065e2170ee0f7e244425c0d0ba30a38776a7aef75e2d5cba0b8b11a950c54' ;; 		s390x) natsArch='s390x'; sha256='23e6ce6b70f9b973106d325eebb8bdd613040bedd4da980ff0aea2d2a7dc122e' ;; 		ppc64le) natsArch='ppc64le'; sha256='5341f41ef6298b05b72dd77c1ec055aeacb1b57dfd600ec888317347b3b4cbf8' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:299c0ee564e4568e71d43a566874e9d853458071d554386ad5728913e55f5d42`  
		Last Modified: Mon, 31 Mar 2025 19:45:06 GMT  
		Size: 6.2 MB (6221370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1af98871a1453d715b201d0cb6c30c2e8240dd12ee7af67f4334bfb80877f3bb`  
		Last Modified: Mon, 31 Mar 2025 19:45:05 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:103d308786c4f17ef7f21746eadc69443e28518b33fd5534040a513bbb5acc64`  
		Last Modified: Mon, 31 Mar 2025 19:45:05 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:261ca6909da20cd9b36804c44211d5a257a4f0a8746e425a8d63cebe1ff274eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bf43f070134532bf9419111138ee6504a3b9010b90d59e6380375b5b9a4abcf`

```dockerfile
```

-	Layers:
	-	`sha256:09877c6dec89674d2ec4aefc8edd75ff573a4834ca2851e1a4be89994ffcd528`  
		Last Modified: Mon, 31 Mar 2025 19:45:05 GMT  
		Size: 14.4 KB (14427 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.21` - linux; s390x

```console
$ docker pull nats@sha256:c14e89986785ed37ac2931d4b307ea84375f49180341e48c9024fe40f226decc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10053962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:893690471f61ea43e10126b7ceb4fd7a07fd98eb86fff95edc6cd8cf10d1e4ef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
ENV NATS_SERVER=2.11.1-binary
# Mon, 31 Mar 2025 17:39:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='2499105f9e64bef55f168f634d34a586b710f6ac041639d8a18364f2b4f4c410' ;; 		armhf) natsArch='arm6'; sha256='31bc11906458e30c8028cdd0301de98713074db73f5e352f58ce4ecd6b1cc641' ;; 		armv7) natsArch='arm7'; sha256='432f4c47cf5adca05da67f1feaf969f6cea50ed9c3bb743a8bb76b8c5c583c8e' ;; 		x86_64) natsArch='amd64'; sha256='827497f99acd54eb0e4e8bfa3b0eb31dd51c6c259110de11a45a7fdacae6c5b3' ;; 		x86) natsArch='386'; sha256='651065e2170ee0f7e244425c0d0ba30a38776a7aef75e2d5cba0b8b11a950c54' ;; 		s390x) natsArch='s390x'; sha256='23e6ce6b70f9b973106d325eebb8bdd613040bedd4da980ff0aea2d2a7dc122e' ;; 		ppc64le) natsArch='ppc64le'; sha256='5341f41ef6298b05b72dd77c1ec055aeacb1b57dfd600ec888317347b3b4cbf8' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67f000d40cf6813dabcb134d2a9b15f3b7eb5ba7dba583ad1df023b35efd9ca`  
		Last Modified: Mon, 31 Mar 2025 19:28:46 GMT  
		Size: 6.6 MB (6585424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4501a9ec92d7d9a89fd0e10cd2ba4c8fb93658a4d46301543d45d1f96b07ce32`  
		Last Modified: Mon, 31 Mar 2025 19:28:45 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06c2b65e72a2a266d2d783396559cd0ee8346a11e25f65ca2b21cc82de4174b6`  
		Last Modified: Mon, 31 Mar 2025 19:28:45 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:82ec15847478c49a8a561d7f21d2239bbea2614e277659456213e6bdd0f5dd49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:443d1aa445d5406aada9c0970885e837d983ea976af12760bad0de2704481f16`

```dockerfile
```

-	Layers:
	-	`sha256:688e4b2d5f0fdef107c3405864e3c9cc14ae13fd320ceddce8f4667dcde9d786`  
		Last Modified: Mon, 31 Mar 2025 19:28:45 GMT  
		Size: 14.4 KB (14360 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:latest`

```console
$ docker pull nats@sha256:76fe53997736051e3511ddc26d585abd679fe3a30dbf74d19418bb0035fde031
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 13
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown
	-	windows version 10.0.17763.7009; amd64

### `nats:latest` - linux; amd64

```console
$ docker pull nats@sha256:0b313c16824b8d98736c06153fa01af3c8d62eebc6298e9062fd2e00c0a3e865
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6282666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5a2333da61b6c9f0de1de8235aca52ee071283b0c8c6487d3ea15b4a0f9f8e2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:54120e60f5a574cbbfd83de2711330ae98499a27ff592bdb694994b87749dd23`  
		Last Modified: Mon, 31 Mar 2025 17:41:30 GMT  
		Size: 6.3 MB (6282155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71d71c31c70e45e814d8db85102321f1459be653c595cd91fafb76306cdf405e`  
		Last Modified: Mon, 31 Mar 2025 19:07:36 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:b8d62bc797363d5eab76aea96ec144d02b901da4dba8eb8bf31cc4e51e3a09d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbd51cd5b25ea5c4355cd2cde0e286d4f6da98802af9ed8b477001ff7ece4679`

```dockerfile
```

-	Layers:
	-	`sha256:19abc39a4cbb247bfa12363ce59bbce1e3bf861fddb9055c3a17e2d39d54d204`  
		Last Modified: Mon, 31 Mar 2025 19:07:36 GMT  
		Size: 10.5 KB (10523 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:af5758489c2981e0a1028dc47f82f0dd2d26e2fac7ac1e478a2a15a12029f6d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6002169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c17f13cf88d7cb6d029eafd34cd847cbacebb2131dc5b7ecfbed791e2958e6a4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:098bda892a4e7ddd77ca838f72ef9757e9b3cfae3c7bc97076a8dd0b6fd92597`  
		Last Modified: Mon, 31 Mar 2025 17:41:30 GMT  
		Size: 6.0 MB (6001660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff1d2651842734b21329c25e1004a4da19102e57001381e60bb4fd58723fe19`  
		Last Modified: Mon, 31 Mar 2025 19:07:08 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:736b8ee8472809de9731d9c426d2113e533e5ac68c9fbf4cd6bb44eb636b3d79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ffa52afcf9f827961f6f692daeb94f398721ac7559f559d56147558f6742150`

```dockerfile
```

-	Layers:
	-	`sha256:cc5887e8b88d73925b5364f9143ca37566f003a1560dffe173f7be8f10d66806`  
		Last Modified: Mon, 31 Mar 2025 19:07:08 GMT  
		Size: 10.7 KB (10650 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:f1752b6d8b3a5506fab1fdf93ce66a6bd6e934d33a3c230231458f254ff505a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5992492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68d3d700cbec0d68868397c08f331e9cee8a3e484035ab651de2414c1bc1039b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7ae07ef7aadc186e26516a3b1a5bacd27b42c41b8d63efc540622587ef29be07`  
		Last Modified: Mon, 31 Mar 2025 17:41:36 GMT  
		Size: 6.0 MB (5991983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d132fb7bc19f6f368e535b5a46903e88d661e5c0f5e33c79b7d66b962039598`  
		Last Modified: Mon, 31 Mar 2025 20:44:23 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:ff00ada993e928a0dbcd0e627e845b5f9c4d11042f0e089912b8ef2969c89876
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab26b373d46f30d56fc9b9ecf02d3c518eb5ab041a8fbb69e562b49b1a864d9d`

```dockerfile
```

-	Layers:
	-	`sha256:d552b4d64ce37965149a8aaeed3a0eebd251066efc77cb63ad2307f9d0bbdef7`  
		Last Modified: Mon, 31 Mar 2025 20:44:23 GMT  
		Size: 10.6 KB (10649 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a360fbbfeb6f19012e875675cf70ea15e5ea3d9e003d5ccf1a61adeed8d515c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5776951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aad8d86003a865c09c995830bd52c9154c44e7976be35a0790b217a28445c6c2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:813138f2f23c3f67c00cc3f899e890b4b46ad187b3c70730ab91bd63ff37fa6d`  
		Last Modified: Mon, 31 Mar 2025 17:41:30 GMT  
		Size: 5.8 MB (5776442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d132fb7bc19f6f368e535b5a46903e88d661e5c0f5e33c79b7d66b962039598`  
		Last Modified: Mon, 31 Mar 2025 20:44:23 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:13fe1989809a4185209660bba2e8a407b921e80a959889e94c8d6b18e6eadc66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cebd7eb7627ea55d24e6c1b36e5124796e00e1a2243414d5b3f65ff44089ec66`

```dockerfile
```

-	Layers:
	-	`sha256:a33f391d8364f479953478aa1b1ce3f8e6e05c31407e5d9ead5d4d5db6da559f`  
		Last Modified: Mon, 31 Mar 2025 20:44:29 GMT  
		Size: 10.7 KB (10708 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; ppc64le

```console
$ docker pull nats@sha256:74e2df57ac704452ee531238216b3accd76025199ee310563732dd2c680227a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5757216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abd71cf45edbcaea354422b03a686d602fac79be9357fdbc6b5c05d8ab8309e5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:452917a8c6e0add88a19efed21ff3bf850d722622f476c3b9d4426f3dbaaffb7`  
		Last Modified: Mon, 31 Mar 2025 17:41:27 GMT  
		Size: 5.8 MB (5756706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc09a85b63b7a6867f196c8c27905ad711a7457fa91d3df80022bc3d24111b3`  
		Last Modified: Mon, 31 Mar 2025 20:07:44 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:9460476db24c3ccd45c6374ab5e0dfa8af2b95e6ed003b294fca69a3f6d49e72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8048c19445dcae5f87494cedbc4822265fb6848963d3958920bc8a77dc19881`

```dockerfile
```

-	Layers:
	-	`sha256:2e79f43f61fe3cbbfb9fa2ab55acbd3a3254d4378c81f4bef4392b1b18e91f10`  
		Last Modified: Mon, 31 Mar 2025 20:07:44 GMT  
		Size: 10.6 KB (10613 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; s390x

```console
$ docker pull nats@sha256:6b9323c60c161cbd82daa5b02f46e55051f8540e7c9770dc1c2ed619086c6f53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6122555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb48b95165c0163d0de0d793f09fa9aaa8dbc79c4b50241ee9e33ac819b1a501`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:cdb5d3b73d4e5760c377e2d1a31f668fd95251ac45157f6a4c4d98139b337e23`  
		Last Modified: Mon, 31 Mar 2025 17:41:31 GMT  
		Size: 6.1 MB (6122046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16e9431fd0e418054b688573b0ef6c205ce09bcb9015c474b01a32d6800912d0`  
		Last Modified: Mon, 31 Mar 2025 20:07:36 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:2dfb1482f9d33c4a0f01a77e40b206f5b997b290b5e3899ee0c2678dd35731a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff58880fe981b8b31c473e8e992460d1ef7a218db9dd4ffc3a951750055bfd3`

```dockerfile
```

-	Layers:
	-	`sha256:9bb52fda18a732bf8f1ead6cd17dd200cfcae43fd84710a4ddb71372c0815f2b`  
		Last Modified: Mon, 31 Mar 2025 20:07:36 GMT  
		Size: 10.5 KB (10523 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - windows version 10.0.17763.7009; amd64

```console
$ docker pull nats@sha256:7523855e64c122a386122c97e7e122f78929c93ef1aaeabcfb818f96108eb526
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.4 MB (113369799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59c769ae1c19e869c3ab50a8bcc53b7a416139faa1f967bef29391891ff94a43`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 05 Mar 2025 21:54:26 GMT
RUN Apply image 10.0.17763.7009
# Mon, 31 Mar 2025 19:16:51 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Mon, 31 Mar 2025 19:16:54 GMT
RUN cmd /S /C #(nop) COPY file:cbd316e46d1e3baa5a0ffb6e227be5b521aa07a7cbe3a0513c0076ac28429bf3 in C:\nats-server.exe 
# Mon, 31 Mar 2025 19:16:55 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Mon, 31 Mar 2025 19:16:55 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Mon, 31 Mar 2025 19:16:56 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 31 Mar 2025 19:16:56 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:543388a101bf4d470af7e8817eff3f6f3b98f13d106939ab3f507a28f2825d0a`  
		Last Modified: Tue, 11 Mar 2025 22:40:48 GMT  
		Size: 106.9 MB (106907688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5764592bce5a260f59c0fc8af513aa702c03e73d61b9d9769cfb463cb5d345a4`  
		Last Modified: Mon, 31 Mar 2025 19:17:00 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c220ae7f5568ad8b19e77200fe2ab8b43bd7e66c8215b73f18cab048bf4c949b`  
		Last Modified: Mon, 31 Mar 2025 19:16:59 GMT  
		Size: 6.5 MB (6456094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24b9abd521fc3bf26173541357dca364e2aaa425fa95150aa12063ad86adbd0f`  
		Last Modified: Mon, 31 Mar 2025 19:16:59 GMT  
		Size: 1.7 KB (1684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47263123c2dca13a6ccd5e6c3f836df870102b1186585b3533a50841169f2d5d`  
		Last Modified: Mon, 31 Mar 2025 19:16:59 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb4c62df8bd6d5f27aca099be80d7290759022e9ed845409d9608b11f0e3db16`  
		Last Modified: Mon, 31 Mar 2025 19:16:58 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faf623903ff066d1e92e2c9250d8f7cd5a3230c1ea39d9cbe269fd63e735f4be`  
		Last Modified: Mon, 31 Mar 2025 19:16:59 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:linux`

```console
$ docker pull nats@sha256:c81104c29f774ab6ac6178391029a857ca1b201750c9ebefad70bee0b9162cf6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:linux` - linux; amd64

```console
$ docker pull nats@sha256:0b313c16824b8d98736c06153fa01af3c8d62eebc6298e9062fd2e00c0a3e865
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6282666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5a2333da61b6c9f0de1de8235aca52ee071283b0c8c6487d3ea15b4a0f9f8e2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:54120e60f5a574cbbfd83de2711330ae98499a27ff592bdb694994b87749dd23`  
		Last Modified: Mon, 31 Mar 2025 17:41:30 GMT  
		Size: 6.3 MB (6282155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71d71c31c70e45e814d8db85102321f1459be653c595cd91fafb76306cdf405e`  
		Last Modified: Mon, 31 Mar 2025 19:07:36 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:b8d62bc797363d5eab76aea96ec144d02b901da4dba8eb8bf31cc4e51e3a09d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbd51cd5b25ea5c4355cd2cde0e286d4f6da98802af9ed8b477001ff7ece4679`

```dockerfile
```

-	Layers:
	-	`sha256:19abc39a4cbb247bfa12363ce59bbce1e3bf861fddb9055c3a17e2d39d54d204`  
		Last Modified: Mon, 31 Mar 2025 19:07:36 GMT  
		Size: 10.5 KB (10523 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:af5758489c2981e0a1028dc47f82f0dd2d26e2fac7ac1e478a2a15a12029f6d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6002169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c17f13cf88d7cb6d029eafd34cd847cbacebb2131dc5b7ecfbed791e2958e6a4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:098bda892a4e7ddd77ca838f72ef9757e9b3cfae3c7bc97076a8dd0b6fd92597`  
		Last Modified: Mon, 31 Mar 2025 17:41:30 GMT  
		Size: 6.0 MB (6001660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff1d2651842734b21329c25e1004a4da19102e57001381e60bb4fd58723fe19`  
		Last Modified: Mon, 31 Mar 2025 19:07:08 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:736b8ee8472809de9731d9c426d2113e533e5ac68c9fbf4cd6bb44eb636b3d79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ffa52afcf9f827961f6f692daeb94f398721ac7559f559d56147558f6742150`

```dockerfile
```

-	Layers:
	-	`sha256:cc5887e8b88d73925b5364f9143ca37566f003a1560dffe173f7be8f10d66806`  
		Last Modified: Mon, 31 Mar 2025 19:07:08 GMT  
		Size: 10.7 KB (10650 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:f1752b6d8b3a5506fab1fdf93ce66a6bd6e934d33a3c230231458f254ff505a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5992492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68d3d700cbec0d68868397c08f331e9cee8a3e484035ab651de2414c1bc1039b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7ae07ef7aadc186e26516a3b1a5bacd27b42c41b8d63efc540622587ef29be07`  
		Last Modified: Mon, 31 Mar 2025 17:41:36 GMT  
		Size: 6.0 MB (5991983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d132fb7bc19f6f368e535b5a46903e88d661e5c0f5e33c79b7d66b962039598`  
		Last Modified: Mon, 31 Mar 2025 20:44:23 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:ff00ada993e928a0dbcd0e627e845b5f9c4d11042f0e089912b8ef2969c89876
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab26b373d46f30d56fc9b9ecf02d3c518eb5ab041a8fbb69e562b49b1a864d9d`

```dockerfile
```

-	Layers:
	-	`sha256:d552b4d64ce37965149a8aaeed3a0eebd251066efc77cb63ad2307f9d0bbdef7`  
		Last Modified: Mon, 31 Mar 2025 20:44:23 GMT  
		Size: 10.6 KB (10649 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a360fbbfeb6f19012e875675cf70ea15e5ea3d9e003d5ccf1a61adeed8d515c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5776951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aad8d86003a865c09c995830bd52c9154c44e7976be35a0790b217a28445c6c2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:813138f2f23c3f67c00cc3f899e890b4b46ad187b3c70730ab91bd63ff37fa6d`  
		Last Modified: Mon, 31 Mar 2025 17:41:30 GMT  
		Size: 5.8 MB (5776442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d132fb7bc19f6f368e535b5a46903e88d661e5c0f5e33c79b7d66b962039598`  
		Last Modified: Mon, 31 Mar 2025 20:44:23 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:13fe1989809a4185209660bba2e8a407b921e80a959889e94c8d6b18e6eadc66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cebd7eb7627ea55d24e6c1b36e5124796e00e1a2243414d5b3f65ff44089ec66`

```dockerfile
```

-	Layers:
	-	`sha256:a33f391d8364f479953478aa1b1ce3f8e6e05c31407e5d9ead5d4d5db6da559f`  
		Last Modified: Mon, 31 Mar 2025 20:44:29 GMT  
		Size: 10.7 KB (10708 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; ppc64le

```console
$ docker pull nats@sha256:74e2df57ac704452ee531238216b3accd76025199ee310563732dd2c680227a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5757216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abd71cf45edbcaea354422b03a686d602fac79be9357fdbc6b5c05d8ab8309e5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:452917a8c6e0add88a19efed21ff3bf850d722622f476c3b9d4426f3dbaaffb7`  
		Last Modified: Mon, 31 Mar 2025 17:41:27 GMT  
		Size: 5.8 MB (5756706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc09a85b63b7a6867f196c8c27905ad711a7457fa91d3df80022bc3d24111b3`  
		Last Modified: Mon, 31 Mar 2025 20:07:44 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:9460476db24c3ccd45c6374ab5e0dfa8af2b95e6ed003b294fca69a3f6d49e72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8048c19445dcae5f87494cedbc4822265fb6848963d3958920bc8a77dc19881`

```dockerfile
```

-	Layers:
	-	`sha256:2e79f43f61fe3cbbfb9fa2ab55acbd3a3254d4378c81f4bef4392b1b18e91f10`  
		Last Modified: Mon, 31 Mar 2025 20:07:44 GMT  
		Size: 10.6 KB (10613 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; s390x

```console
$ docker pull nats@sha256:6b9323c60c161cbd82daa5b02f46e55051f8540e7c9770dc1c2ed619086c6f53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6122555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb48b95165c0163d0de0d793f09fa9aaa8dbc79c4b50241ee9e33ac819b1a501`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:cdb5d3b73d4e5760c377e2d1a31f668fd95251ac45157f6a4c4d98139b337e23`  
		Last Modified: Mon, 31 Mar 2025 17:41:31 GMT  
		Size: 6.1 MB (6122046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16e9431fd0e418054b688573b0ef6c205ce09bcb9015c474b01a32d6800912d0`  
		Last Modified: Mon, 31 Mar 2025 20:07:36 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:2dfb1482f9d33c4a0f01a77e40b206f5b997b290b5e3899ee0c2678dd35731a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff58880fe981b8b31c473e8e992460d1ef7a218db9dd4ffc3a951750055bfd3`

```dockerfile
```

-	Layers:
	-	`sha256:9bb52fda18a732bf8f1ead6cd17dd200cfcae43fd84710a4ddb71372c0815f2b`  
		Last Modified: Mon, 31 Mar 2025 20:07:36 GMT  
		Size: 10.5 KB (10523 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:nanoserver`

```console
$ docker pull nats@sha256:ab7919f36b0bf7f8b85e92aadeb04b95a0f3a5f1d2b33203d2ed60c8104ef5ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `nats:nanoserver` - windows version 10.0.17763.7009; amd64

```console
$ docker pull nats@sha256:7523855e64c122a386122c97e7e122f78929c93ef1aaeabcfb818f96108eb526
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.4 MB (113369799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59c769ae1c19e869c3ab50a8bcc53b7a416139faa1f967bef29391891ff94a43`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 05 Mar 2025 21:54:26 GMT
RUN Apply image 10.0.17763.7009
# Mon, 31 Mar 2025 19:16:51 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Mon, 31 Mar 2025 19:16:54 GMT
RUN cmd /S /C #(nop) COPY file:cbd316e46d1e3baa5a0ffb6e227be5b521aa07a7cbe3a0513c0076ac28429bf3 in C:\nats-server.exe 
# Mon, 31 Mar 2025 19:16:55 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Mon, 31 Mar 2025 19:16:55 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Mon, 31 Mar 2025 19:16:56 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 31 Mar 2025 19:16:56 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:543388a101bf4d470af7e8817eff3f6f3b98f13d106939ab3f507a28f2825d0a`  
		Last Modified: Tue, 11 Mar 2025 22:40:48 GMT  
		Size: 106.9 MB (106907688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5764592bce5a260f59c0fc8af513aa702c03e73d61b9d9769cfb463cb5d345a4`  
		Last Modified: Mon, 31 Mar 2025 19:17:00 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c220ae7f5568ad8b19e77200fe2ab8b43bd7e66c8215b73f18cab048bf4c949b`  
		Last Modified: Mon, 31 Mar 2025 19:16:59 GMT  
		Size: 6.5 MB (6456094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24b9abd521fc3bf26173541357dca364e2aaa425fa95150aa12063ad86adbd0f`  
		Last Modified: Mon, 31 Mar 2025 19:16:59 GMT  
		Size: 1.7 KB (1684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47263123c2dca13a6ccd5e6c3f836df870102b1186585b3533a50841169f2d5d`  
		Last Modified: Mon, 31 Mar 2025 19:16:59 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb4c62df8bd6d5f27aca099be80d7290759022e9ed845409d9608b11f0e3db16`  
		Last Modified: Mon, 31 Mar 2025 19:16:58 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faf623903ff066d1e92e2c9250d8f7cd5a3230c1ea39d9cbe269fd63e735f4be`  
		Last Modified: Mon, 31 Mar 2025 19:16:59 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver-1809`

```console
$ docker pull nats@sha256:ab7919f36b0bf7f8b85e92aadeb04b95a0f3a5f1d2b33203d2ed60c8104ef5ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `nats:nanoserver-1809` - windows version 10.0.17763.7009; amd64

```console
$ docker pull nats@sha256:7523855e64c122a386122c97e7e122f78929c93ef1aaeabcfb818f96108eb526
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.4 MB (113369799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59c769ae1c19e869c3ab50a8bcc53b7a416139faa1f967bef29391891ff94a43`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 05 Mar 2025 21:54:26 GMT
RUN Apply image 10.0.17763.7009
# Mon, 31 Mar 2025 19:16:51 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Mon, 31 Mar 2025 19:16:54 GMT
RUN cmd /S /C #(nop) COPY file:cbd316e46d1e3baa5a0ffb6e227be5b521aa07a7cbe3a0513c0076ac28429bf3 in C:\nats-server.exe 
# Mon, 31 Mar 2025 19:16:55 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Mon, 31 Mar 2025 19:16:55 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Mon, 31 Mar 2025 19:16:56 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 31 Mar 2025 19:16:56 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:543388a101bf4d470af7e8817eff3f6f3b98f13d106939ab3f507a28f2825d0a`  
		Last Modified: Tue, 11 Mar 2025 22:40:48 GMT  
		Size: 106.9 MB (106907688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5764592bce5a260f59c0fc8af513aa702c03e73d61b9d9769cfb463cb5d345a4`  
		Last Modified: Mon, 31 Mar 2025 19:17:00 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c220ae7f5568ad8b19e77200fe2ab8b43bd7e66c8215b73f18cab048bf4c949b`  
		Last Modified: Mon, 31 Mar 2025 19:16:59 GMT  
		Size: 6.5 MB (6456094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24b9abd521fc3bf26173541357dca364e2aaa425fa95150aa12063ad86adbd0f`  
		Last Modified: Mon, 31 Mar 2025 19:16:59 GMT  
		Size: 1.7 KB (1684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47263123c2dca13a6ccd5e6c3f836df870102b1186585b3533a50841169f2d5d`  
		Last Modified: Mon, 31 Mar 2025 19:16:59 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb4c62df8bd6d5f27aca099be80d7290759022e9ed845409d9608b11f0e3db16`  
		Last Modified: Mon, 31 Mar 2025 19:16:58 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faf623903ff066d1e92e2c9250d8f7cd5a3230c1ea39d9cbe269fd63e735f4be`  
		Last Modified: Mon, 31 Mar 2025 19:16:59 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:scratch`

```console
$ docker pull nats@sha256:c81104c29f774ab6ac6178391029a857ca1b201750c9ebefad70bee0b9162cf6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:scratch` - linux; amd64

```console
$ docker pull nats@sha256:0b313c16824b8d98736c06153fa01af3c8d62eebc6298e9062fd2e00c0a3e865
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6282666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5a2333da61b6c9f0de1de8235aca52ee071283b0c8c6487d3ea15b4a0f9f8e2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:54120e60f5a574cbbfd83de2711330ae98499a27ff592bdb694994b87749dd23`  
		Last Modified: Mon, 31 Mar 2025 17:41:30 GMT  
		Size: 6.3 MB (6282155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71d71c31c70e45e814d8db85102321f1459be653c595cd91fafb76306cdf405e`  
		Last Modified: Mon, 31 Mar 2025 19:07:36 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:b8d62bc797363d5eab76aea96ec144d02b901da4dba8eb8bf31cc4e51e3a09d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbd51cd5b25ea5c4355cd2cde0e286d4f6da98802af9ed8b477001ff7ece4679`

```dockerfile
```

-	Layers:
	-	`sha256:19abc39a4cbb247bfa12363ce59bbce1e3bf861fddb9055c3a17e2d39d54d204`  
		Last Modified: Mon, 31 Mar 2025 19:07:36 GMT  
		Size: 10.5 KB (10523 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:af5758489c2981e0a1028dc47f82f0dd2d26e2fac7ac1e478a2a15a12029f6d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6002169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c17f13cf88d7cb6d029eafd34cd847cbacebb2131dc5b7ecfbed791e2958e6a4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:098bda892a4e7ddd77ca838f72ef9757e9b3cfae3c7bc97076a8dd0b6fd92597`  
		Last Modified: Mon, 31 Mar 2025 17:41:30 GMT  
		Size: 6.0 MB (6001660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff1d2651842734b21329c25e1004a4da19102e57001381e60bb4fd58723fe19`  
		Last Modified: Mon, 31 Mar 2025 19:07:08 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:736b8ee8472809de9731d9c426d2113e533e5ac68c9fbf4cd6bb44eb636b3d79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ffa52afcf9f827961f6f692daeb94f398721ac7559f559d56147558f6742150`

```dockerfile
```

-	Layers:
	-	`sha256:cc5887e8b88d73925b5364f9143ca37566f003a1560dffe173f7be8f10d66806`  
		Last Modified: Mon, 31 Mar 2025 19:07:08 GMT  
		Size: 10.7 KB (10650 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:f1752b6d8b3a5506fab1fdf93ce66a6bd6e934d33a3c230231458f254ff505a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5992492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68d3d700cbec0d68868397c08f331e9cee8a3e484035ab651de2414c1bc1039b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7ae07ef7aadc186e26516a3b1a5bacd27b42c41b8d63efc540622587ef29be07`  
		Last Modified: Mon, 31 Mar 2025 17:41:36 GMT  
		Size: 6.0 MB (5991983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d132fb7bc19f6f368e535b5a46903e88d661e5c0f5e33c79b7d66b962039598`  
		Last Modified: Mon, 31 Mar 2025 20:44:23 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:ff00ada993e928a0dbcd0e627e845b5f9c4d11042f0e089912b8ef2969c89876
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab26b373d46f30d56fc9b9ecf02d3c518eb5ab041a8fbb69e562b49b1a864d9d`

```dockerfile
```

-	Layers:
	-	`sha256:d552b4d64ce37965149a8aaeed3a0eebd251066efc77cb63ad2307f9d0bbdef7`  
		Last Modified: Mon, 31 Mar 2025 20:44:23 GMT  
		Size: 10.6 KB (10649 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a360fbbfeb6f19012e875675cf70ea15e5ea3d9e003d5ccf1a61adeed8d515c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5776951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aad8d86003a865c09c995830bd52c9154c44e7976be35a0790b217a28445c6c2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:813138f2f23c3f67c00cc3f899e890b4b46ad187b3c70730ab91bd63ff37fa6d`  
		Last Modified: Mon, 31 Mar 2025 17:41:30 GMT  
		Size: 5.8 MB (5776442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d132fb7bc19f6f368e535b5a46903e88d661e5c0f5e33c79b7d66b962039598`  
		Last Modified: Mon, 31 Mar 2025 20:44:23 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:13fe1989809a4185209660bba2e8a407b921e80a959889e94c8d6b18e6eadc66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cebd7eb7627ea55d24e6c1b36e5124796e00e1a2243414d5b3f65ff44089ec66`

```dockerfile
```

-	Layers:
	-	`sha256:a33f391d8364f479953478aa1b1ce3f8e6e05c31407e5d9ead5d4d5db6da559f`  
		Last Modified: Mon, 31 Mar 2025 20:44:29 GMT  
		Size: 10.7 KB (10708 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:74e2df57ac704452ee531238216b3accd76025199ee310563732dd2c680227a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5757216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abd71cf45edbcaea354422b03a686d602fac79be9357fdbc6b5c05d8ab8309e5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:452917a8c6e0add88a19efed21ff3bf850d722622f476c3b9d4426f3dbaaffb7`  
		Last Modified: Mon, 31 Mar 2025 17:41:27 GMT  
		Size: 5.8 MB (5756706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc09a85b63b7a6867f196c8c27905ad711a7457fa91d3df80022bc3d24111b3`  
		Last Modified: Mon, 31 Mar 2025 20:07:44 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:9460476db24c3ccd45c6374ab5e0dfa8af2b95e6ed003b294fca69a3f6d49e72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8048c19445dcae5f87494cedbc4822265fb6848963d3958920bc8a77dc19881`

```dockerfile
```

-	Layers:
	-	`sha256:2e79f43f61fe3cbbfb9fa2ab55acbd3a3254d4378c81f4bef4392b1b18e91f10`  
		Last Modified: Mon, 31 Mar 2025 20:07:44 GMT  
		Size: 10.6 KB (10613 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; s390x

```console
$ docker pull nats@sha256:6b9323c60c161cbd82daa5b02f46e55051f8540e7c9770dc1c2ed619086c6f53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6122555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb48b95165c0163d0de0d793f09fa9aaa8dbc79c4b50241ee9e33ac819b1a501`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:cdb5d3b73d4e5760c377e2d1a31f668fd95251ac45157f6a4c4d98139b337e23`  
		Last Modified: Mon, 31 Mar 2025 17:41:31 GMT  
		Size: 6.1 MB (6122046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16e9431fd0e418054b688573b0ef6c205ce09bcb9015c474b01a32d6800912d0`  
		Last Modified: Mon, 31 Mar 2025 20:07:36 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:2dfb1482f9d33c4a0f01a77e40b206f5b997b290b5e3899ee0c2678dd35731a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff58880fe981b8b31c473e8e992460d1ef7a218db9dd4ffc3a951750055bfd3`

```dockerfile
```

-	Layers:
	-	`sha256:9bb52fda18a732bf8f1ead6cd17dd200cfcae43fd84710a4ddb71372c0815f2b`  
		Last Modified: Mon, 31 Mar 2025 20:07:36 GMT  
		Size: 10.5 KB (10523 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:windowsservercore`

```console
$ docker pull nats@sha256:9d03bcf6cbd1a06b72b01b12931276f9f11d428800308790ac7d2c5e7f013153
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `nats:windowsservercore` - windows version 10.0.17763.7009; amd64

```console
$ docker pull nats@sha256:358cd0aed79a204ff4c8b5c055a03c487c5358d7455e0ffa579125eceef0d34e
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2158788658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ee73222ac79929936f4b58dc26a22b9521b1d61e7a78f7c5ed88a75f23f1374`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 05 Mar 2025 22:09:20 GMT
RUN Install update 10.0.17763.7009
# Mon, 31 Mar 2025 18:52:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 31 Mar 2025 18:52:57 GMT
ENV NATS_DOCKERIZED=1
# Mon, 31 Mar 2025 18:52:58 GMT
ENV NATS_SERVER=2.11.1-binary
# Mon, 31 Mar 2025 18:52:59 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.1-binary/nats-server-v2.11.1-binary-windows-amd64.zip
# Mon, 31 Mar 2025 18:52:59 GMT
ENV NATS_SERVER_SHASUM=2ab6b2c964fd5fe3b10a471cba309033f0756182f69228a65d1764197facf59c
# Mon, 31 Mar 2025 18:53:46 GMT
RUN Set-PSDebug -Trace 2
# Mon, 31 Mar 2025 18:54:06 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Mon, 31 Mar 2025 18:54:06 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Mon, 31 Mar 2025 18:54:07 GMT
EXPOSE 4222 6222 8222
# Mon, 31 Mar 2025 18:54:08 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 31 Mar 2025 18:54:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77bec5e4bac3c7f6dc5d56da5ffc11e72881485b3a55330c17c915ad653f955`  
		Last Modified: Tue, 11 Mar 2025 17:48:06 GMT  
		Size: 431.4 MB (431366277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35a6c48e83b6ecc670f12e09411b9f19d7fb0a878e1f86a6812563467340ff8`  
		Last Modified: Mon, 31 Mar 2025 18:54:13 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c158e67ae1fa853b1e146c6dd4e2b8f7e13aab94075904e788f4dfa3b8943322`  
		Last Modified: Mon, 31 Mar 2025 18:54:12 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6610f67e82d540d4cf11d12f87f1a68f8b42e4371905c52df1cade737e4f44c`  
		Last Modified: Mon, 31 Mar 2025 18:54:11 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0929886be3ca1628c185214c762369ea53c4afb47d0603d3d69fb4b471d01bf7`  
		Last Modified: Mon, 31 Mar 2025 18:54:12 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a89f7e18c6f6e8406fbe811630282ddd985e8899085b73506a0f39ac3c8fcf33`  
		Last Modified: Mon, 31 Mar 2025 18:54:11 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a904ed39f5ad31d12b93284fed611d377be64b1d3871e896c2e1c83415ff28`  
		Last Modified: Mon, 31 Mar 2025 18:54:11 GMT  
		Size: 333.8 KB (333807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5239d01ea32c2be9edfc2b25b142685efcbaedbadb1778166b52c0858df66464`  
		Last Modified: Mon, 31 Mar 2025 18:54:11 GMT  
		Size: 6.8 MB (6807873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56c6af05e936d2967cd915bd57f5faacef8b514317cd4de730f837f728d14487`  
		Last Modified: Mon, 31 Mar 2025 18:54:10 GMT  
		Size: 1.9 KB (1931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe56937824b786b5d064fe15be3435e14f26a022d00662003396c61194954e0`  
		Last Modified: Mon, 31 Mar 2025 18:54:10 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4aaffd9d1722fd09e9a67ad18073b6716178658c1f5517404d7b4180df3142f`  
		Last Modified: Mon, 31 Mar 2025 18:54:10 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdcbf0f98ff7504665d65ee0034ca94a89e45d2ecc47f808f87787d51427d265`  
		Last Modified: Mon, 31 Mar 2025 18:54:10 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-1809`

```console
$ docker pull nats@sha256:9d03bcf6cbd1a06b72b01b12931276f9f11d428800308790ac7d2c5e7f013153
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `nats:windowsservercore-1809` - windows version 10.0.17763.7009; amd64

```console
$ docker pull nats@sha256:358cd0aed79a204ff4c8b5c055a03c487c5358d7455e0ffa579125eceef0d34e
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2158788658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ee73222ac79929936f4b58dc26a22b9521b1d61e7a78f7c5ed88a75f23f1374`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 05 Mar 2025 22:09:20 GMT
RUN Install update 10.0.17763.7009
# Mon, 31 Mar 2025 18:52:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 31 Mar 2025 18:52:57 GMT
ENV NATS_DOCKERIZED=1
# Mon, 31 Mar 2025 18:52:58 GMT
ENV NATS_SERVER=2.11.1-binary
# Mon, 31 Mar 2025 18:52:59 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.1-binary/nats-server-v2.11.1-binary-windows-amd64.zip
# Mon, 31 Mar 2025 18:52:59 GMT
ENV NATS_SERVER_SHASUM=2ab6b2c964fd5fe3b10a471cba309033f0756182f69228a65d1764197facf59c
# Mon, 31 Mar 2025 18:53:46 GMT
RUN Set-PSDebug -Trace 2
# Mon, 31 Mar 2025 18:54:06 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Mon, 31 Mar 2025 18:54:06 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Mon, 31 Mar 2025 18:54:07 GMT
EXPOSE 4222 6222 8222
# Mon, 31 Mar 2025 18:54:08 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 31 Mar 2025 18:54:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77bec5e4bac3c7f6dc5d56da5ffc11e72881485b3a55330c17c915ad653f955`  
		Last Modified: Tue, 11 Mar 2025 17:48:06 GMT  
		Size: 431.4 MB (431366277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35a6c48e83b6ecc670f12e09411b9f19d7fb0a878e1f86a6812563467340ff8`  
		Last Modified: Mon, 31 Mar 2025 18:54:13 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c158e67ae1fa853b1e146c6dd4e2b8f7e13aab94075904e788f4dfa3b8943322`  
		Last Modified: Mon, 31 Mar 2025 18:54:12 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6610f67e82d540d4cf11d12f87f1a68f8b42e4371905c52df1cade737e4f44c`  
		Last Modified: Mon, 31 Mar 2025 18:54:11 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0929886be3ca1628c185214c762369ea53c4afb47d0603d3d69fb4b471d01bf7`  
		Last Modified: Mon, 31 Mar 2025 18:54:12 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a89f7e18c6f6e8406fbe811630282ddd985e8899085b73506a0f39ac3c8fcf33`  
		Last Modified: Mon, 31 Mar 2025 18:54:11 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a904ed39f5ad31d12b93284fed611d377be64b1d3871e896c2e1c83415ff28`  
		Last Modified: Mon, 31 Mar 2025 18:54:11 GMT  
		Size: 333.8 KB (333807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5239d01ea32c2be9edfc2b25b142685efcbaedbadb1778166b52c0858df66464`  
		Last Modified: Mon, 31 Mar 2025 18:54:11 GMT  
		Size: 6.8 MB (6807873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56c6af05e936d2967cd915bd57f5faacef8b514317cd4de730f837f728d14487`  
		Last Modified: Mon, 31 Mar 2025 18:54:10 GMT  
		Size: 1.9 KB (1931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe56937824b786b5d064fe15be3435e14f26a022d00662003396c61194954e0`  
		Last Modified: Mon, 31 Mar 2025 18:54:10 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4aaffd9d1722fd09e9a67ad18073b6716178658c1f5517404d7b4180df3142f`  
		Last Modified: Mon, 31 Mar 2025 18:54:10 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdcbf0f98ff7504665d65ee0034ca94a89e45d2ecc47f808f87787d51427d265`  
		Last Modified: Mon, 31 Mar 2025 18:54:10 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
