print("Yoga Guider developed by Monty")
experience = input("Enter your yoga experience (beginner/intermediate/advanced): ").lower()
flexibility = input("Enter your body flexibility (good/bad): ").lower()

basic = {
    "Tadasana": ("Stand straight with arms up", "Improves posture and balance"),
    "Vajrasana": ("Sit on knees and keep spine straight", "Improves digestion"),
    "Bhujangasana": ("Lie on stomach and lift chest", "Strengthens spine"),
    "Balasana": ("Sit back and stretch arms forward", "Reduces stress"),
    "Tree Pose": ("Stand on one leg and balance", "Improves focus")
}

intermediate = {
    "Warrior Pose": ("Step one leg forward and stretch arms", "Builds strength"),
    "Triangle Pose": ("Stretch legs and touch foot sideways", "Improves flexibility"),
    "Bridge Pose": ("Lift hips while lying down", "Strengthens back"),
    "Boat Pose": ("Balance on hips and lift legs", "Strengthens core"),
    "Seated Twist": ("Twist upper body while seated", "Improves digestion")
}

advanced = {
    "Crow Pose": ("Balance body on hands", "Builds arm strength"),
    "Headstand": ("Balance body on head and arms", "Improves blood circulation"),
    "Wheel Pose": ("Lift body into backbend", "Increases spine flexibility"),
    "Handstand": ("Balance body upside down", "Builds full body strength"),
    "Scorpion Pose": ("Arch back while inverted", "Improves balance and flexibility")
}

print("\n--- Yoga Pose Plan ---\n")

def show_poses(level, poses):
    print(level)
    for pose, info in poses.items():
        print(pose)
        print("How to perform:", info[0])
        print("Benefits:", info[1])
        print()

if experience == "beginner" or flexibility == "bad":
    show_poses("Basic Yoga Poses", basic)

elif experience == "intermediate":
    show_poses("Basic Yoga Poses", basic)
    show_poses("Intermediate Yoga Poses", intermediate)

elif experience == "advanced" and flexibility == "good":
    show_poses("Basic Yoga Poses", basic)
    show_poses("Intermediate Yoga Poses", intermediate)
    show_poses("Advanced Yoga Poses", advanced)

else:
    print("Invalid input please enter correct details")
