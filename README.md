# Kafka Performance Optimization - Lab Guides
**Hands-On Labs for "Optimize Kafka for Speed & Availability" Course**

---

## 📚 Overview

This repository contains three comprehensive lab guides designed to accompany the "Optimize Kafka for Speed & Availability" video course. Through hands-on exercises, you'll learn to configure, monitor, and optimize Apache Kafka clusters for production use.

**Total Time:** ~3 hours of hands-on practice  
**Prerequisites:** Basic familiarity with command-line terminals and Docker  
**Tools Required:** Docker Desktop (8GB+ RAM recommended)

---

## 🎯 Learning Path

### **[Module 1: Configure Topics for High Availability](module-1-guide.md)**
⏱️ **60 minutes** | 📊 **Difficulty:** Beginner

Learn to configure Kafka topics with appropriate replication factors, partition counts, and durability settings to ensure high availability and fault tolerance.

**What You'll Learn:**
- Create topics with replication for zero-downtime during failures
- Calculate optimal partition counts based on throughput requirements
- Apply production configuration patterns for different use cases

**Labs Included:**
- Lab 1: Replication Factors and Data Durability
- Lab 2: Partition Strategy for Parallelism
- Lab 3: Topic Configuration Best Practices

**[Start Module 1 →](module-1-guide.md)**

---

### **[Module 2: Monitor Performance and Identify Bottlenecks](module-2-guide.md)**
⏱️ **60 minutes** | 📊 **Difficulty:** Intermediate

Master consumer lag monitoring, consumer group sizing, and broker health metrics to identify and diagnose performance bottlenecks before they impact production.

**What You'll Learn:**
- Monitor and interpret consumer lag metrics
- Calculate optimal consumer group sizes based on partition count
- Diagnose performance bottlenecks using broker health indicators
- Set up alerting for critical metrics

**Labs Included:**
- Lab 1: Understanding Consumer Lag
- Lab 2: Consumer Group Sizing and Parallelism
- Lab 3: Broker Health Monitoring

**[Start Module 2 →](module-2-guide.md)**

---

### **[Module 3: Optimize Producer and Consumer Performance](module-3-guide.md)**
⏱️ **90 minutes** | 📊 **Difficulty:** Advanced

Optimize Kafka performance through producer batching, compression, consumer fetch tuning, and broker-side configuration to maximize throughput while meeting latency SLAs.

**What You'll Learn:**
- Optimize producer configurations for maximum throughput
- Compare compression algorithms and select the best for your use case
- Tune consumer fetch settings to prevent timeouts
- Understand broker-side threading and buffer configurations

**Labs Included:**
- Lab 1: Producer Batching and Compression
- Lab 2: Consumer Fetch Optimization
- Lab 3: Broker-Side Performance Tuning

**[Start Module 3 →](module-3-guide.md)**

---

## 🚀 Quick Start

### Prerequisites

1. **Install Docker Desktop**
   - [Mac](https://docs.docker.com/desktop/install/mac-install/)
   - [Windows](https://docs.docker.com/desktop/install/windows-install/)
   - [Linux](https://docs.docker.com/desktop/install/linux-install/)

2. **Allocate Resources to Docker**
   - Minimum: 8GB RAM, 4 CPUs
   - Recommended: 12GB RAM, 6 CPUs
   - Docker Desktop → Settings → Resources

### Set Up Your Lab Environment

Each module guide includes detailed setup instructions. Here's the quick version:

```bash
# Create working directory
mkdir -p ~/kafka-labs
cd ~/kafka-labs

# Download docker-compose.yml from Module 1 guide
# (Full instructions in module-1-guide.md)

# Start Kafka cluster
docker-compose up -d

# Wait for cluster to start
sleep 60

# Verify it's running
docker-compose ps
```

**Detailed setup instructions** are provided in [Module 1](module-1-guide.md#lab-environment-setup).

---

## 📖 How to Use These Guides

### Study Approach

1. **Watch the video** for the module (if available)
2. **Read the "Key Concepts"** section to understand theory
3. **Work through each lab exercise** hands-on
4. **Complete the quiz** to test your understanding
5. **Move to the next module**

### Lab Format

Each lab includes:
- 🎯 **Learning objectives** - What you'll master
- 💡 **Key concepts** - Theory explained simply
- ⚙️ **Hands-on exercises** - Step-by-step commands
- ❓ **Questions to answer** - Test your understanding
- ✅ **Key takeaways** - Remember these!

---

## 🛠️ What You'll Build

By the end of these labs, you'll have:

- ✅ Configured a 3-broker Kafka cluster with Docker
- ✅ Created production-ready topics with replication and partitioning
- ✅ Monitored consumer lag and broker health
- ✅ Sized consumer groups for optimal parallelism
- ✅ Optimized producer throughput by 3-5x through batching and compression
- ✅ Tuned consumer fetch settings to prevent timeouts
- ✅ Set up monitoring and alerting rules

**Final Project:** Build and optimize a complete Kafka system for an e-commerce platform processing 100,000 orders/day.

---

## 📊 Skills Progression

```
Module 1: Configure     →  Module 2: Monitor      →  Module 3: Optimize
├─ Replication          →  ├─ Consumer lag        →  ├─ Producer batching
├─ Partitions           →  ├─ Consumer groups     →  ├─ Compression
└─ Topic configs        →  └─ Broker health       →  └─ Fetch tuning
                                                      
Beginner                   Intermediate              Advanced
```

---

## 🎓 Learning Outcomes

After completing all three modules, you will be able to:

1. **Configure** Kafka topics with appropriate replication factors, partition counts, and durability settings
2. **Monitor** consumer lag, broker health, and identify performance bottlenecks
3. **Optimize** producer and consumer configurations for maximum throughput while meeting latency SLAs
4. **Design** production-ready Kafka architectures that balance availability, performance, and cost
5. **Troubleshoot** common Kafka performance issues using metrics and diagnostic tools

---

## 💼 Real-World Applications

These skills are used by:

- **Netflix** - 700+ billion events/day using 36 Kafka clusters
- **LinkedIn** - 7+ trillion messages/day through 100+ clusters
- **Uber** - Real-time dispatch and surge pricing optimization
- **Walmart** - 100 million SKUs/day inventory synchronization

**Learn more:** Case studies and examples are included throughout the guides.

---

## 🧪 Lab Environment

### What's Included

- **3-broker Kafka cluster** (using Confluent Platform 7.5.0)
- **Zookeeper** for coordination
- **Command-line tools** for topic management, producers, consumers
- **Performance testing tools** (`kafka-producer-perf-test`)

### Architecture

```
┌─────────────────────────────────────────┐
│         Your Computer (Docker)          │
├─────────────────────────────────────────┤
│  ┌──────────┐  ┌──────────┐  ┌──────────┐
│  │ Broker 1 │  │ Broker 2 │  │ Broker 3 │
│  │ :9092    │  │ :9093    │  │ :9094    │
│  └──────────┘  └──────────┘  └──────────┘
│       │             │             │        
│  ┌────────────────────────────────────┐  
│  │        Zookeeper :2181            │  
│  └────────────────────────────────────┘  
└─────────────────────────────────────────┘
```

---

## 📚 Additional Resources

### Official Documentation
- [Apache Kafka Documentation](https://kafka.apache.org/documentation/)
- [Confluent Platform Documentation](https://docs.confluent.io/)

### Performance Guides
- [Kafka Performance Tuning](https://www.redpanda.com/guides/kafka-performance-kafka-performance-tuning)
- [Consumer Lag Monitoring](https://docs.confluent.io/platform/current/monitor/monitor-consumer-lag.html)
- [Partition Strategies](https://www.confluent.io/blog/how-choose-number-topics-partitions-kafka-cluster/)

### Community
- [Kafka Users Mailing List](https://kafka.apache.org/contact)
- [Confluent Community Slack](https://launchpass.com/confluentcommunity)
- [Stack Overflow: apache-kafka](https://stackoverflow.com/questions/tagged/apache-kafka)

---

## 🤝 Contributing

Found an issue or have a suggestion? 

- **Report bugs:** Open an issue describing the problem
- **Suggest improvements:** Open an issue with your idea
- **Fix typos:** Submit a pull request

---

## 📝 Course Information

These lab guides accompany the **"Optimize Kafka for Speed & Availability"** course.

- **Duration:** 60 minutes (videos) + 3 hours (hands-on labs)
- **Level:** Intermediate
- **Instructor:** [Your Name]
- **Prerequisites:** Basic understanding of distributed systems and command-line usage

---

## ⚖️ License

This educational material is provided as-is for learning purposes.

Apache Kafka and related trademarks are property of the Apache Software Foundation.

---

## 🎯 Getting Started

Ready to begin? Start with Module 1:

**[→ Begin Module 1: Configure Topics for High Availability](module-1-guide.md)**

---

## 📞 Support

**Need help?**
- Review the troubleshooting sections in each module guide
- Check the [Additional Resources](#additional-resources) section
- Ask questions in the course discussion forum

---

## ✅ Module Completion Checklist

Track your progress:

- [ ] **Module 1:** Configured topics with replication and partitioning
- [ ] **Module 1:** Passed quiz (4/5 correct)
- [ ] **Module 2:** Monitored consumer lag and sized consumer groups
- [ ] **Module 2:** Passed quiz (4/5 correct)
- [ ] **Module 3:** Optimized producer and consumer performance
- [ ] **Module 3:** Passed quiz (4/5 correct)
- [ ] **Final Project:** Built complete e-commerce Kafka system
- [ ] **Certification:** Ready to earn your Kafka certification!

---

## 🚀 What's Next?

After completing these labs:

1. **Apply to real projects** - Use Kafka in your applications
2. **Explore advanced topics** - Kafka Streams, ksqlDB, Schema Registry
3. **Get certified** - Confluent Certified Developer for Apache Kafka
4. **Join the community** - Contribute to open source, help others learn

---

**Happy Learning! 🎉**

*Last Updated: November 2024*
