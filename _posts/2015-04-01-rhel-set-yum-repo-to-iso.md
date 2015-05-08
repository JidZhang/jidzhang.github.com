---
layout: post
title: "RHEL 5.x ������ָ��ΪYUM������"
description: "RHEL 5.x ����ν�����ָ��ΪYUM������"
category: �ٶ�,Linux
tags: [YUM]
---
{% include JB/setup %}

������һ�£�ȷʵ�ǿ��Խ����̾�����Ϊyum�İ�װ������������ϲ����rhel���˻��ǱȽϷ���ġ�������Ҳ���Խ����°汾��rhel�����������Ʒ���yum upgradeʵ�ְ汾���¡�

1. mount -o loop rhel-5-server-dvd.iso /media/rhel

2. vi /etc/yum.repos.d/rhel-local.repo

	[Cluster]
	name=Red Hat Enterprise Linux $releasever - $basearch - Cluster
	baseurl=file:///media/rhel/Cluster
	enabled=1
	gpgcheck=1
	gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-redhat-release

	[ClusterStorage]
	name=Red Hat Enterprise Linux $releasever - $basearch - ClusterStorage
	baseurl=file:///media/rhel/ClusterStorage
	enabled=1
	gpgcheck=1
	gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-redhat-release

	[Server]
	name=Red Hat Enterprise Linux $releasever - $basearch - Server
	baseurl=file:///media/rhel/Server
	enabled=1
	gpgcheck=1
	gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-redhat-release

	[VT]
	name=Red Hat Enterprise Linux $releasever - $basearch - VT
	baseurl=file:///media/rhel/VT
	enabled=1
	gpgcheck=1
	gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-redhat-release

3. mkdir -p /var/rhel/{Cluster,ClusterStorage,Server,VT}

4. createrepo
	createrepo -o /var/rhel/Cluster -g /media/rhel/Cluster/repodata/comps-rhel5-cluster.xml /media/rhel/Cluster
	createrepo -o /var/rhel/ClusterStorage -g /media/rhel/ClusterStorage/repodata/comps-rhel5-cluster-st.xml /media/rhel/ClusterStorage
	createrepo -o /var/rhel/Server -g /media/rhel/Server/repodata/comps-rhel5-server-core.xml /media/rhel/Server
	createrepo -o /var/rhel/VT -g /media/rhel/VT/repodata/comps-rhel5-vt.xml /media/rhel/VT

5. mount 
	mount --bind /var/rhel/Cluster/repodata /media/rhel/Cluster/repodata
	mount --bind /var/rhel/ClusterStorage/repodata /media/rhel/ClusterStorage/repodata
	mount --bind /var/rhel/Server/repodata /media/rhel/Server/repodata
	mount --bind /var/rhel/VT/repodata /media/rhel/VT/repodata

6. yum clean all