## `nats:2-scratch`

```console
$ docker pull nats@sha256:bb90d21b87ba223e838d39e5ee66ebeea8b63e8a6bffb4a2b19f5b291e46d1fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:2-scratch` - linux; amd64

```console
$ docker pull nats@sha256:6fb1a85021a8411e0470cca8a43d461db915d2df605657389c4f0595d2e42e91
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5548142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8780d448219e4996eb219326ba6943b7e05f04ab1189a6f1dcf2e013058e3e36`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 13 Mar 2024 01:47:57 GMT
COPY file:33d3e4ce6e17dc907ca0b478996354d26d433431b7bf48ae5bef3ec2ea1359f1 in /nats-server 
# Wed, 13 Mar 2024 01:47:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 13 Mar 2024 01:47:57 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 01:47:57 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 13 Mar 2024 01:47:57 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ce8539fabe7af34129953a073c64515d008d19eac52a820ef52368f6411e540d`  
		Last Modified: Wed, 13 Mar 2024 01:48:46 GMT  
		Size: 5.5 MB (5547633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5208dae10516783bd9b5be071d7f3d39c84e1138b3887856c85f570ec4f588c`  
		Last Modified: Wed, 13 Mar 2024 01:48:45 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:b717fb731a88e81bdabf9b7eb28e2ee0fa423ff801dcd5819fb4ffaf217cb208
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5263761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f51552a7d22c2c5ca2447ff2b4198de16cfdff9a116a3c54ef5af0d997a9469f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 13 Mar 2024 00:49:35 GMT
COPY file:c24c6855bab6e8b64a222738f44249dd58afe5ec56a34cfd64493e736f5325df in /nats-server 
# Wed, 13 Mar 2024 00:49:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 13 Mar 2024 00:49:35 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 00:49:35 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 13 Mar 2024 00:49:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bc2b5fa4421ea8f446fd52c0a8e7c8c6e048dc4aa6a096fb60765aa281147267`  
		Last Modified: Wed, 13 Mar 2024 00:50:20 GMT  
		Size: 5.3 MB (5263253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:652cf78472b592b1ea355485d1a353340ba41c0d01b26f15ffacc090db84d7bb`  
		Last Modified: Wed, 13 Mar 2024 00:50:19 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:07d02d1f567ff67a36ece1f90364e466f099db860d2e8ec1f2143bec1c3710f4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5255037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5956a4e3835d4532ea5cbfc23f7b2e2d96d15a877f42392feea63afa16be107b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 13 Mar 2024 00:35:52 GMT
COPY file:6899efa16d7091375dc53de2fc1e5686e82569d9799d6cede2e40b0a8b6abb48 in /nats-server 
# Wed, 13 Mar 2024 00:35:52 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 13 Mar 2024 00:35:52 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 00:35:52 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 13 Mar 2024 00:35:52 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:68296288971fdb3ddfe9bfba9b6a79725a69e891fb82cd5708f088afaac9929f`  
		Last Modified: Wed, 13 Mar 2024 00:36:43 GMT  
		Size: 5.3 MB (5254529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:652026202bce83174144280de06b0537518e9d13e1674ac88f0d7e8491a2e440`  
		Last Modified: Wed, 13 Mar 2024 00:36:42 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:f8017338e2c0dd9d3adb17672dd8226d475d5c810fa5f742c27a1d77f6e0c0e7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5117686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8216507954fc8ffbaa79f3aa0908756fb3b5e699a13215671cf23837d30ca343`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 13 Mar 2024 00:40:40 GMT
COPY file:674069719b01a345db55aa1ea35485a8b6f0cf0eed465ae05a0c00073e2ab2ab in /nats-server 
# Wed, 13 Mar 2024 00:40:40 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 13 Mar 2024 00:40:40 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 00:40:40 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 13 Mar 2024 00:40:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d5466aeaf1139b432e415e6412234c167a91220e74d17f50be1a2de5b0fb1b21`  
		Last Modified: Wed, 13 Mar 2024 00:41:26 GMT  
		Size: 5.1 MB (5117178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:562c0bd40d1b70ec911e4b7219f7867675e2ad1c67899a3643f13d261d792187`  
		Last Modified: Wed, 13 Mar 2024 00:41:25 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:e964ace9a5047268966aa2f1f2e10472325f21ac790016722c0a9090997a39f1
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5097257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57a273f9d6d6aa560ff8df97aee7e4c13f87044f2be0081b07ba0f4a0fafd81a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 16 Feb 2024 19:24:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 13 Mar 2024 01:29:00 GMT
COPY file:0e1c98477f605478a27423b67d1c7bf88d4b2a56d0696ea31430a8a59b294dd8 in /nats-server 
# Wed, 13 Mar 2024 01:29:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 13 Mar 2024 01:29:01 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 01:29:01 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 13 Mar 2024 01:29:02 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7eaf17599ba122502fe00d1cb4014722df0b46a83f614f9430f71b816a6999f8`  
		Last Modified: Wed, 13 Mar 2024 01:29:44 GMT  
		Size: 5.1 MB (5096748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9b8d7d148d9f2f60c0b13204daf3a2f76ff85991d79fe4fd82aa842a3d77a1d`  
		Last Modified: Wed, 13 Mar 2024 01:29:43 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; s390x

```console
$ docker pull nats@sha256:21d23f9777f88070c60ce8bf669dd9169ad10d91ddae1f43c02b5419cc5fcbc6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5430830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45a9daecac5ba461be180b94ca61fe053ebe1e5c23af8e61522f1854982e6157`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 11 Jan 2024 17:54:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 13 Mar 2024 01:15:09 GMT
COPY file:cc94c349de0e266f428d63773845fb669334304c5fbcffeec57553d333126f22 in /nats-server 
# Wed, 13 Mar 2024 01:15:09 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 13 Mar 2024 01:15:09 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 01:15:09 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 13 Mar 2024 01:15:09 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0bf838b872f1e012c580bbff8d1e66a09a7b05a85651db222851ea3323dab3d2`  
		Last Modified: Wed, 13 Mar 2024 01:16:47 GMT  
		Size: 5.4 MB (5430321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:668de88817078f4ef2cf284dff428f40567f94b7132efee56fe3abe6264e6d42`  
		Last Modified: Wed, 13 Mar 2024 01:16:46 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
